# Micro-Frontend with Angular

This repository demonstrates implementing a Micro-Frontend architecture using Angular with a Monorepo workspace.

## Steps to Implement Micro-Frontend

1. **Create Workspace**:  
   ```bash
   npx @angular/cli@18 new mono-repo-workspace --create-application=false
   ```

2. **Generate Applications**:  
   - Host Application:  
     ```bash
     ng g application host-app --routing --style=scss
     ```
   - Remote Application:  
     ```bash
     ng g application mfe-app --routing --style=scss
     ```

3. **Add Module Federation**:  
   - Host (Port: 4200):  
     ```bash
     ng add @angular-architects/module-federation --project host-app --port 4200 --type host
     ```
   - Remote (Port: 4300):  
     ```bash
     ng add @angular-architects/module-federation --project mfe-app --port 4300 --type remote
     ```

4. **Serve Applications**:  
   - Host Application:  
     ```bash
     ng serve host-app -o
     ```
   - Remote Application:  
     ```bash
     ng serve mfe-app -o
     

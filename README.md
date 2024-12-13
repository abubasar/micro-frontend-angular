# Micro Frontend Angular

Here i implement micro-frontend with mono repo workspace approach.

## Step by step command to implement micro-frontend

### Run `npx @angular/cli@18 new mono-repo-workspace --create-application=false` for creating angular blank application in angular 18.

### Run `ng g application host-app --routing --style=scss` for creating host application.
### Run `ng g application mfe-app --routing --style=scss` for creating remote application.

### Run `ng serve host-app -o` to run host application.
### Run `ng serve mfe-app -o` to run remote application.

### Run `ng add @angular-architects/module-federation --project host-app --port 4200 --type host` to add module federation in host application assigning default port 4200.
### Run `ng add @angular-architects/module-federation --project mfe-app --port 4300 --type remote` to add module federation in remote application assigning default port 4300.

### Run `ng serve host-app -o` to run host application again.
### Run `ng serve mfe-app -o` to run remote application again.

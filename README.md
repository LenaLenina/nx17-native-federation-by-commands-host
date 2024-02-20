npm install -g @angular/cli

npx create-nx-workspace host --preset=apps

cd host

npm install --save-dev @nx/angular

npx nx g @nx/angular:app host --skipTests --directory 'apps/host' --style scss --bundler esbuild --e2eTestRunner none --projectNameAndRootFormat as-provided

npm install @angular-architects/native-federation

npx nx g @angular-architects/native-federation:ng-add

npx nx serve host -o

npx nx build host

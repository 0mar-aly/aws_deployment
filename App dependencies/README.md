# App dependencies
The project mainly uses Node.js and Express for the API, Angular for the frontend, and Sequelize for database connection. The detailed list of dependencies is found below.

## API/Backend
```
  "dependencies": {
    "@types/bcrypt": "^3.0.1",
    "@types/jsonwebtoken": "^8.5.8",
    "aws-sdk": "^2.1108.0",
    "bcrypt": "^5.0.1",
    "body-parser": "^1.20.0",
    "cors": "^2.8.5",
    "dotenv": "^8.2.0",
    "email-validator": "^2.0.4",
    "express": "^4.17.3",
    "jsonwebtoken": "^8.5.1",
    "path": "^0.12.7",
    "pg": "^8.7.1",
    "reflect-metadata": "^0.1.13",
    "sequelize": "^5.22.5",
    "sequelize-typescript": "^0.6.11"
  },
  "devDependencies": {
    "@types/bluebird": "^3.5.36",
    "@types/cors": "^2.8.12",
    "@types/express": "^4.17.13",
    "@types/node": "^11.15.54",
    "@types/sequelize": "^4.28.11",
    "@types/validator": "^10.11.3",
    "@typescript-eslint/eslint-plugin": "^2.34.0",
    "@typescript-eslint/parser": "^2.34.0",
    "chai": "^4.3.6",
    "chai-http": "^4.3.0",
    "eslint": "^6.8.0",
    "eslint-config-google": "^0.14.0",
    "mocha": "^6.2.3",
    "ts-node-dev": "^1.1.8",
    "typescript": "^3.9.10"
  }
  ```

  ## Frontend
  ```
    "dependencies": {
    "@angular/common": "^8.2.14",
    "@angular/core": "^8.2.14",
    "@angular/forms": "^8.2.14",
    "@angular/http": "^7.2.2",
    "@angular/platform-browser": "^8.2.14",
    "@angular/platform-browser-dynamic": "^8.2.14",
    "@angular/router": "^8.2.14",
    "@ionic-native/core": "^5.0.0",
    "@ionic-native/splash-screen": "^5.0.0",
    "@ionic-native/status-bar": "^5.0.0",
    "@ionic/angular": "^4.1.0",
    "core-js": "^2.5.4",
    "rxjs": "~6.5.4",
    "zone.js": "~0.9.1"
  },
  "devDependencies": {
    "@angular-devkit/architect": "^0.1303.1",
    "@angular-devkit/build-angular": "^0.803.24",
    "@angular-devkit/core": "~7.2.3",
    "@angular-devkit/schematics": "~7.2.3",
    "@angular/cli": "~8.3.25",
    "@angular/compiler": "~8.2.14",
    "@angular/compiler-cli": "~8.2.14",
    "@angular/language-service": "~8.2.14",
    "@ionic/angular-toolkit": "~1.4.0",
    "@types/jasmine": "~2.8.8",
    "@types/jasminewd2": "~2.0.3",
    "@types/node": "~10.12.0",
    "@typescript-eslint/eslint-plugin": "^2.20.0",
    "@typescript-eslint/parser": "^2.20.0",
    "codelyzer": "~4.5.0",
    "jasmine-core": "~2.99.1",
    "jasmine-spec-reporter": "~4.2.1",
    "karma": "~3.1.4",
    "karma-chrome-launcher": "~2.2.0",
    "karma-coverage-istanbul-reporter": "~2.0.1",
    "karma-firefox-launcher": "^2.1.2",
    "karma-jasmine": "~1.1.2",
    "karma-jasmine-html-reporter": "^0.2.2",
    "protractor": "~5.4.0",
    "ts-node": "~8.0.0",
    "tslint": "~5.12.0",
    "typescript": "^3.5.3"
  }
  ```
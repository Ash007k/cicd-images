FROM cypress/browsers:node14.17.6-chrome100-ff98

LABEL maintainer="jinjie" \
      description="Image used for running Cypress testing framework"
    
RUN npm install -g cypress mysql \
                   mocha mocha-steps mochawesome mochawesome-merge \
                   mochawesome-report-generator \
                   cypress-eslint-preprocessor \
                   cypress-promise \
                   cypress-xpath \
                   eslint faker@5.5.3 fs-extra moment prettier dotenv \
                   lodash date-fns cypress-fail-fast

COPY ./version-info /usr/bin

RUN chmod +x /usr/bin/version-info

RUN npm link $(ls -1 $(npm root -g)/)

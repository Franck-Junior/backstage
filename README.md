
# [Backstage](https://backstage.io)

This is your newly scaffolded Backstage App, Good Luck!

To start the app, run:

```sh
yarn install
yarn dev
```

## Docker Deployment

```sh
yarn install --frozen-lockfile

# tsc outputs type definitions to dist-types/ in the repo root, which are then consumed by the build
yarn tsc

# Build all packages and in the end bundle them all up into the packages/backend/dist folder.
yarn build

docker image build . -f packages/backend/Dockerfile --tag backstage

docker run -it -p 7007:7007 backstage
```

You should then start to get logs in your terminal, and then you can open your browser at `http://localhost:7007`


https://github.com/backstage/backstage/blob/618d78495cf6cdf8928365a20b97435c5a65074d/packages/backend-common/src/service/lib/hostFactory.ts

https://github.com/backstage/backstage/blob/c6cc3ccc74d77b6aeba038f5c316e997ccf4452b/packages/backend-common/src/service/lib/ServiceBuilderImpl.ts

https://github.com/backstage/backstage/blob/618d78495cf6cdf8928365a20b97435c5a65074d/packages/backend-common/src/service/lib/config.ts
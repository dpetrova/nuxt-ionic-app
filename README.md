# Nuxt 3 Minimal Starter

Look at the [Nuxt 3 documentation](https://nuxt.com/docs/getting-started/introduction) to learn more.

## Setup

Make sure to install the dependencies:

```bash
# npm
npm install

# pnpm
pnpm install

# yarn
yarn install

# bun
bun install
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# npm
npm run dev

# pnpm
pnpm run dev

# yarn
yarn dev

# bun
bun run dev
```

## Production

Build the application for production:

```bash
# npm
npm run build

# pnpm
pnpm run build

# yarn
yarn build

# bun
bun run build
```

Locally preview production build:

```bash
# npm
npm run preview

# pnpm
pnpm run preview

# yarn
yarn preview

# bun
bun run preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.

## Setup Capacitor

1. Install Ionic CLI globally with:

```bash
# npm
npm install -g @ionic/cli

# yarn
yarn global add @ionic/cli
```

2. Enable Capacitor:

```bash
# ionic cli
ionic integrations enable capacitor

# npx
npx @ionic/cli integrations enable capacitor
```

3. Add the Android and/or iOS platform(s):

```bash
# ionic cli
ionic capacitor add ios
ionic capacitor add android

# npx
npx @ionic/cli capacitor add ios
npx @ionic/cli capacitor add android
```

4. There are system requirements for building and running iOS and Android apps locally. See the Capacitor environment setup documentation for more details.

## Native Builds with Capacitor

1. Create a web build:

```bash
# npm
npm run generate

# npx
npx nuxi generate
#or:
npx nuxi build
```

2. Update your Capacitor project directories with your latest app build:

```bash
npx cap sync
```

3. Run the app from the command line using an installed device OR:

- You must set in Environment variable JAVA_HOME the path found in:
  File -> Settings -> Build, Execution, Deployment -> Build Tools -> Gradle JDK
  - Something like:
    JAVA_HOME=D:\Android\Android Studio\jbr

```bash
npx cap run android
npx cap run ios
```

4. (Optional) Open the project in Android Studio or XCode, respectively:

```bash
npx cap open android
npx cap open ios
```

## Deploying with Appflow

1. Start by creating a repository in the Git provider of your choice and pushing your local project to the remote repository
2. Log in or create an account at ionic.io to get started with Appflow
3. Import an existing app and select the repository for your Nuxt project.
4. Once connected, you’ll see the most recent commit in the Commits screen in Appflow. Select ‘Start build’ from the latest commit.
5. This brings you to the build screen. Select the Android platform, and the default latest Build stack and Debug build type will pre-select. For this build type, no signing certificates, custom environments, or native configs are needed.
6. This kicks off the process for a cloud native build of the app for Android devices. Once the build is complete, you can download the .apk and .aab files to run in an emulator or on a device.
7. When your app is ready for a production build, you can store signing certificates, provisioning profiles, and app store credentials in Appflow to easily build and deploy for end users.

Check out the [deployment documentation](https://ionic.io/docs/appflow/quickstart/github) for more information.

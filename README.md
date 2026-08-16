## Get started

1. Install dependencies

   ```bash
   npm install
   ```

2. Start the app

   ```bash
   npx expo start
   ```

In the output, you'll find options to open the app in a

- [development build](https://docs.expo.dev/develop/development-builds/introduction/)
- [Android emulator](https://docs.expo.dev/workflow/android-studio-emulator/)
- [iOS simulator](https://docs.expo.dev/workflow/ios-simulator/)
- [Expo Go](https://expo.dev/go), a limited sandbox for trying out app development with Expo

You can start developing by editing the files inside the **app** directory. This project uses [file-based routing](https://docs.expo.dev/router/introduction).

- To set up ESLint for linting, run `npx expo lint`, or follow our guide on ["Using ESLint and Prettier"](https://docs.expo.dev/guides/using-eslint/)
- If you'd like to set up unit testing, follow our guide on ["Unit Testing with Jest"](https://docs.expo.dev/develop/unit-testing/)
- Learn more about the TypeScript setup in this template in our guide on ["Using TypeScript"](https://docs.expo.dev/guides/typescript/)

# CI/CD pipelins :

Pull request
→ lint
→ format check
→ TypeScript check
→ unit tests
→ coverage
→ dependency scan
→ secret scan
→ SAST/code quality
→ Android debug build

Main branch
→ all PR checks
→ Android release build
→ iOS build
→ artifact signing
→ deploy to internal testing

Release tag
→ production build
→ manual approval
→ Play Store / App Store deployment

# Tools

CI/CD: GitHub Actions.

Linting: ESLint.

Formatting: Prettier.

Type checking: tsc --noEmit.

Tests: Jest and React Native Testing Library.

Coverage: Jest coverage.

Dependency vulnerabilities: npm audit, Dependabot, or Snyk.

Dependency review: GitHub Dependency Review Action.

SAST/code quality: CodeQL or SonarQube.

Secret scanning: GitHub secret scanning or Gitleaks.

Android build: Gradle.

iOS build: Xcode/Fastlane.

Mobile distribution: Firebase App Distribution, TestFlight, and Play Console internal testing.

Crash monitoring: Firebase Crashlytics or Sentry.

Important additions
Also include:

Dependency pinning: commit package-lock.json or yarn.lock.

SBOM generation: useful for tracking supply-chain dependencies.

License checks: detect incompatible package licenses.

Signed builds: keep Android keystore and App Store credentials in protected GitHub secrets.

Environment separation: development, staging, and production.

Manual production approval: do not deploy directly from every commit.

Build caching: cache npm, Gradle, and CocoaPods dependencies.

Branch protection: require CI checks and code review before merging.

E2E tests: use Detox against a staging backend before release.

API compatibility tests: ensure the app works with the deployed backend.

OTA updates carefully: use Expo Updates or CodePush only for JavaScript changes, not native changes.

# Repro local native module crash

```
yarn install
eas build -e production -p android

```

## The error in the android build
```
FAILURE: Build failed with an exception.
* What went wrong:
Execution failed for task ':my-module:compileReleaseKotlin'.
> 'compileReleaseJavaWithJavac' task (current target is 17) and 'compileReleaseKotlin' task (current target is 11) jvm target compatibility should be set to the same Java version.
  Consider using JVM toolchain: https://kotl.in/gradle/jvm/toolchain
```
https://expo.dev/accounts/reachvote/projects/repro-module-build-error/builds/d32df12e-5d73-4f28-81a1-c07993e3929f

## How I created the module

```
npx create-expo-module@next --local
```
accept all defaults
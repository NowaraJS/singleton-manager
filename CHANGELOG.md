
## v1.1.10

[compare changes](https://github.com/NowaraJS/singleton-manager/compare/v1.1.9...v1.1.10)

### 🧹 Refactors

- **🧹:** [Rename error keys for consistency] Updated the error key constants in the SingletonManager to follow a consistent naming convention. The previous keys were renamed from `singletonManagerErrorKeys` to `SINGLETON_MANAGER_ERROR_KEYS` to enhance readability and maintainability. This change affects the enums and the corresponding references in the SingletonManager and its tests. ([50bc6ae](https://github.com/NowaraJS/singleton-manager/commit/50bc6ae))

### 📖 Documentation

- **📖:** [Add Copilot instructions for development workflow] ([18c966f](https://github.com/NowaraJS/singleton-manager/commit/18c966f))

### 📦 Build

- **📦:** [Update TypeScript and peer dependency versions] ## Build Changes - Updated TypeScript from version ^5.8.3 to ^5.9.2 - Updated @nowarajs/error from version ^1.1.2 to ^1.1.4 ([54a6619](https://github.com/NowaraJS/singleton-manager/commit/54a6619))
- **📦:** [Update include path in TypeScript build config] ([e7a7a0b](https://github.com/NowaraJS/singleton-manager/commit/e7a7a0b))
- **📦:** [Remove unused entry point from build configuration] - Removed the entry point './source/enums/index.ts' from the build configuration as it is no longer needed. ([400115d](https://github.com/NowaraJS/singleton-manager/commit/400115d))

### 🦉 Chore

- **🦉:** [Remove outdated changelog entries] ([db809a2](https://github.com/NowaraJS/singleton-manager/commit/db809a2))

### 🤖 CI

- **🤖:** [Add Copilot setup workflow for automated steps] ([b1c80e9](https://github.com/NowaraJS/singleton-manager/commit/b1c80e9))

### ❤️ Contributors

- Komiroko <komiriko@pm.me>


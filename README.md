# 🎯 NowaraJS - Singleton Manager

## 📌 Table of Contents

- [🎯 Singleton Manager](#-singleton-manager)
	- [📌 Table of Contents](#-table-of-contents)
	- [📝 Description](#-description)
	- [✨ Features](#-features)
	- [🔧 Installation](#-installation)
	- [⚙️ Usage](#-usage)
	- [📚 API Reference](#-api-reference)
	- [⚖️ License](#-license)
	- [📧 Contact](#-contact)

## 📝 Description

> A powerful and type-safe singleton manager for TypeScript/JavaScript applications.

**Singleton Manager** provides a centralized way to manage singleton instances in your application. It ensures that only one instance of each registered class exists throughout the application lifecycle, with full TypeScript support and type safety.

## ✨ Features

- 🔒 **Type-safe**: Full TypeScript support with generics
- 🎯 **Centralized Management**: Single registry for all your singletons
- ⚡ **Lightweight**: Minimal overhead with maximum functionality

## 🔧 Installation

```bash
bun add @nowarajs/singleton-manager @nowarajs/error
```

## ⚙️ Usage

```typescript
import { SingletonManager } from '@nowarajs/singleton-manager';

// Define your singleton classes
class DatabaseConnection {
	private _isConnected = false;

	public constructor() {
		console.log('Database connection created');
		this._isConnected = true;
	}

	public query(sql: string): string[] {
		console.log(`Executing query: ${sql}`);
		return ['result1', 'result2'];
	}
}

class ApiClient {
	public constructor(
		private readonly _baseUrl: string,
		private readonly _apiKey: string
	) {}

	public get baseUrl(): string {
		return this._baseUrl;
	}
}

// Register singletons (with or without constructor parameters)
SingletonManager.register('DatabaseConnection', new DatabaseConnection());
SingletonManager.register('ApiClient', new ApiClient('https://api.example.com', 'key'));

// Get singleton instances (same instance every time)
const db1 = SingletonManager.get<DatabaseConnection>('DatabaseConnection');
const db2 = SingletonManager.get<DatabaseConnection>('DatabaseConnection');
console.log(db1 === db2); // true

// TypeScript provides full type safety
db1.query('SELECT * FROM users'); // ✅ Works
// db1.nonExistentMethod(); // ❌ TypeScript error

// Check if registered
if (SingletonManager.has('ApiClient')) {
	const client = SingletonManager.get<ApiClient>('ApiClient');
	console.log(client.baseUrl); // https://api.example.com
}

// Unregister and re-register
SingletonManager.unregister('DatabaseConnection');
SingletonManager.register('DatabaseConnection', new DatabaseConnection());
```

## 📚 API Reference

You can find the complete API reference documentation for `SingletonManager` at:

- [Reference Documentation](https://nowarajs.github.io/singleton-manager/)

## ⚖️ License

Distributed under the MIT License. See [LICENSE](./LICENSE) for more information.

## 📧 Contact

- Mail: [nowarajs@pm.me](mailto:nowarajs@pm.me)
- GitHub: [NowaraJS](https://github.com/NowaraJS)
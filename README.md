# engined-notification

Notification service for engined, used to send notification in backend.


## Installation

Install via NPM:

```shell
npm install engined-notification
```

## Usage

Start engined-notification service in engined, see example below:

```javascript
const { Manager } = require('engined');
const NotificationService = require('engined-notification');

const notification = NotificationService();

const main = async () => {

	// Create manager
	let serviceManager = new Manager({ verbose: true });

	// Adding service to manager
	serviceManager.add('Notification', notification);

	// Start all services
	await serviceManager.startAll();
};

main();
```

## Using specific notification backend

Here is example to get agent for specific backend to save file:

```javascript

// Using local notification backend
let localAgent = this.getContext('Notification').getAgent('local');

```

## Register notification backend

```javascript

// Register notification backend
this.getContext('Notification').registerAgent('local', agent);
```

## License
Licensed under the MIT License

## Authors
Copyright(c) 2017 Leon Lin（林為志） <<leonlin14@gmail.com>>

# raspiot
a framework for IoT project running on Raspberry Pi
# Structure

### Installation
```sh
pip install raspiot
```

### Component

a physical device in two types

- Generator
    - generate data
- Reactor
    - perform actions in react to data changes

```Python
Component:
	config()
	
	Generator:
		send()
	Reactor:
		react()
```

### Worker

responsible for handling data generate from components; authentication, data transfer, etc.

```Python
Worker:
	configure()
	work()
```

### Pipeline

a bridge to transfer data from worker to component or from component to worker.

- publish() : publish data to pipeline
- subscribe() : when data has changed, call the function that workers or components provide.

```Python
Pipeline:
	publish()
	subscribe()
```

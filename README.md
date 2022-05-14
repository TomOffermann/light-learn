# light-learn
Simple machine learning library written in TypeScript for NodeJS or client-side applications. There is no dependency on any modules or libraries.

## Main Applications:
* Pattern recognition
* Image classification

## Getting started:
```console
$ mkdir <project> && cd ./<project>
$ npm init -y
$ git clone https://github.com/TomOffermann/light-learn
```

## Create an entry point:

```javascript
import { Net, Dense, Dataset } from "light-learn";

const input = [1, 2, 3, 4, 5, 6, 20, 30, 45, 100];
const output = [2, 4, 6, 8, 10, 12, 40, 60, 90, 200];

const data = [50, 90, 3, 0, -2]

const dataset = new Dataset(input, output);

const myNet = new Net(new Dense(256));
myNet.add(new Dense(2))

myNet.train(dataset, 2000, 0.01);
console.log(myNet.predict(data));
```
```console
$ node <entry point>
[100, 180, 6, 0, -4]
```

# plantuml

Convert [PlantUML] diagram text to SVG.

> Using PlantUML Version 1.2023.2

## Installation

```bash
$ npm install nishidemasami/plantuml
```

## Dependencies

Requires java and graphviz to be installed on the system.

## Usage

```js
const plantuml = require('plantuml');
const svg = await plantuml(`
  @startuml
  Bob -> Alice : hello
  Alice -> Wonderland: hello
  Wonderland -> next: hello
  next -> Last: hello
  Last -> next: hello
  next -> Wonderland : hello
  Wonderland -> Alice : hello
  Alice -> Bob: hello
  @enduml
`);

require('fs').writeFileSync('image.svg', svg);
```

## License

MIT

[PlantUML]: https://plantuml.com
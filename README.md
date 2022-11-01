# @datasco/serializer
Public node.js data serializer (XML, HTML, CSV, TSV), written in TypeScript.

# Installation
To install serializer via NPM:
```bash
npm i @datasco/serializer
```

# How to use

## Serialize XML
```ts
import { XMLSerializer } from '@datasco/serializer'

const obj: Record<string, any> = {
  product: [
    {
      $data: { accuracy: 1 },
      text: [
        { raw: 'Hello' },
        { raw: 'World' }
      ]
    },
    {
      $data: { accuracy: 0.6 },
      text: [
        { raw: 'Hello' },
        { raw: 'World' }
      ]
    }
  ]
}

console.log(XMLSerializer.serialize(obj, { root: 'data', attrs: '$data' ))
/*
<data>
  <product accuracy="1">
    <text>
      <raw>Hello</raw>
    </text>
    <text>
      <raw>World</raw>
    </text>
  </product>
  <product accuracy="0.6">
    <text>
      <raw>Hello</raw>
    </text>
    <text>
      <raw>World</raw>
    </text>
  </product>
</data>
*/
```

## Serialize CSV/TSV
In progress.

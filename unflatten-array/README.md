# unflatten

Unflatten complex structures including arrays and objects!

## Install

```bash
$ npm i --save unflatten-array
```

## Usage

```js
const complexFlattenedData = {
  "[0].email": "sambhavjain2612@gmail.com",
  "[0].name.first": "Sambhav",
  "[0].name.last": "Jain",
  "[0].meta.status": "ACTIVE",
  "[0].meta.permissionsGranted": true,
  "[1].skills[0].category": "Frontend",
  "[1].skills[0].value": "React.js",
  "[1].skills[1].category": "Backend",
  "[1].skills[1].value": "Node.js",
};
const unflattenArray = require("unflatten-array");
unflattenArray(complexFlattenedData);

/* logs ->
[
  {
    email: 'sambhavjain2612@gmail.com',
    name: { first: 'Sambhav', last: 'Jain' },
    meta: { status: 'ACTIVE', permissionsGranted: true }
  },
  { 
    skills: [
      {category: "Frontend", value: "React.js"}, 
      {category: "Backend", value: "Node.js"}
    ]
  }
]
*/
```

#### Released under MIT License
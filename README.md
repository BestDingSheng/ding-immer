# ding-immer

个人项目实现了 immer 的核心功能

## Install

```bahs
npm install ding-immer
```

## Example 

```js 

import { produce } from './immer'

const baseState = {
  name: 'dingsheng',
  list: ['1'],
};

const nextState = produce(baseState, draft => {
  draft.list.push('2');
});


console.log(baseState); // {name: 'dingsheng' , list: ['1']},
console.log(nextState) // {name: 'dingsheng' , list: ['1', '2']},
console.log(baseState === nextState) // false

```
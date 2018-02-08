# SimpleUI

## Use

```javascript
// import part of components
import Vue from "vue";
import {Header, Button, ...} from "./simpleUI";

Vue.component(Header.name, Header);
Vue.component(Button.name, Button);
...

// full import
import SimpleUI from "./simpleUI"l

Vue.use(SimpleUI);
```

---

## Button

name: "sp-button"

#### params:

- color: (default | black | blue | yellow | red)
- size: (small | default | big)

#### use:

```html
<sp-button color="blue" size="small">
    Confirm
</sp-button>
```

## Header

name: "sp-header"

#### params:

- title
- lett
- right

#### use:

```html
<sp-header>
    <span slot="left">back</span>
    <span slot="title">title</span>
    <span slot="right">options</span>
</sp-header>
```

## Toggle

name: "sp-toggle"

#### params:

* @param {array} items
* @param {string} color (white | black)
* @param {string} panelColor (white | black)

#### use:

```html
<template>
    <sp-toggle :items="items" panelColor="black" color="white"/>
</template>

<script>
    data(){
        return{
            items: [
                {
                    name: "home",
                    to: "/home"
                },
                {
                    name: "posts",
                    to: "/posts"
                }
            ]
        }
    }
</script>
```

## Message

name: "sp-message"

#### params

* @param {string} message
* @param {boolean} messageShow
* @param {string} cancle btn
* @event messageHandler

#### use:

```html
<sp-message 
    :messageShow="messageShow"
    @messageHandler="messagehandler" 
    cancle="true" 
    message="网络请求发生错误，请刷新页面重试..."
/>
```
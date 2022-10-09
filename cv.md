# RS School CV

## Samuel Jędrzejewski

### Contact information

* **E-mail address:** samijedrzejewski@gmail.com
* **Phone number:** XXX XXX XXX
* **Discord:** 238SAMIxD#2054

### My summary

Junior Software Engineer, Web Developer - JavaScript/TypeScript, Computer Science student, Startup Front-End Engineer, Volunteer, Partner. I mostly use those programming languages: JavaScript (also HTML and CSS) in React with TypeScript, PHP, SQL, C++, Java, C#, Swift. I have also created simple mobile applications as well as I am editing some videos. Besides university classes I was making fully functional website service of the chess tournament with register, login, signing systems and using external APIs and what is more my own REST API that would allow other developers accessing data about games and players in their apps. I am additionally learning Unity engine to develop and publish my very first video game in horror/hacking type. I am attending many IT conferences, meetings, webinars and actively taking part in volunteering.

### Skills

* HTML
* CSS
* JavaScript
* React
* TypeScript
* Git
* Markdown
* Node
* npm
* REST

### Code examples

* **Quick sort:**

```js
const items = [5,3,7,6,2,9];

function swap(items, leftIndex, rightIndex){
    var temp = items[leftIndex];
    items[leftIndex] = items[rightIndex];
    items[rightIndex] = temp;
}

function partition(items, left, right) {
    let pivot = items[Math.floor((right + left) / 2)],
        i = left,
        j = right;
    while (i <= j) {
        while (items[i] < pivot) {
            i++;
        }
        while (items[j] > pivot) {
            j--;
        }
        if (i <= j) {
            swap(items, i, j);
            i++;
            j--;
        }
    }
    return i;
}

function quickSort(items, left, right) {
    let index;
    if (items.length > 1) {
        index = partition(items, left, right);
        if (left < index - 1) {
            quickSort(items, left, index - 1);
        }
        if (index < right) {
            quickSort(items, index, right);
        }
    }
    return items;
}

const sortedArray = quickSort(items, 0, items.length - 1);
console.log(sortedArray);
```

* **Euklid's algorithm:**

```js
const num1 = 252;
const num2 = 105;
const findGCD = (num1, num2) => {
   let a = Math.abs(num1);
   let b = Math.abs(num2);
   while (a && b && a !== b) {
      if(a > b){
         [a, b] = [a - b, b];
      }else{
         [a, b] = [a, b - a];
      };
   };
   return a || b;
};
console.log(findGCD(num1, num2));
```

* **Smartphone payment application *CCS only*:**

```html
<input type="radio" name="tab" id="terminal" value="terminal" class="hidden radio1" checked />
<input type="radio" name="tab" id="payment" value="payment" class="hidden radio2" />
<input type="radio" name="tab" id="settings" value="settings" class="hidden radio3" />
<input type="radio" name="tab" id="topayment" value="topayment" class="hidden radio4" />
<div class="content">
 <div class="phone">
  <div class="border">
   <span class="volume up"></span>
   <span class="volume down"></span>
   <span class="camera">
    <span class="lens"></span>
   </span>
   <span class="detectors">
    <span class="light"></span>
    <span class="motion"></span>
   </span>
   <span class="speaker"></span>
   <span class="logo"></span>
   <div class="screen">
    <div class="statusbar">
     <span class="icon i1"></span>
     <span class="icon i2"></span>
     <span class="icon i3"></span>
     <span class="icon nfc"></span>
     <span class="icon wifi"></span>
     <span class="icon coverage"></span>
     <span class="procent">97%</span>
     <span class="icon battery"></span>
     <span class="time">11:34</span>
    </div>
    <div class="application">
     <div class="terminal-content">
      <div class="amount">
       <p>€</p>
       231,43
      </div>
      <div class="keyboard">
       <div>
        <p>1</p>
        <p>4</p>
        <p>7</p>
        <p>*</p>
        <p class="cancel"></p>
       </div>
       <div>
        <p>2</p>
        <p>5</p>
        <p>8</p>
        <p>0</p>
        <p class="undo"></p>
       </div>
       <div>
        <p>3</p>
        <p>6</p>
        <p>9</p>
        <p>#</p>
        <p class="accept"></p>
       </div>
      </div>
     </div>
     <div class="payment-content">
      <p class="no-payment">No incoming payments</p>
      <p>Place the phone near terminal</p>
      <span class="money"></span>
     </div>
     <div class="to-payment-content">
      <p class="no-payment">Incoming payment</p>
      <p>Do you confirm incoming payment?</p>
      <p>
       Zgraj się
       <br />
       Shopping
       <br />
       2,38 €
       <div class="to-payment">
                <label for="payment">
                  <p class="reject"></p>
                </label>
        <label for="payment">
                  <p class="okay"></p>
                </label>
       </div>
      </p>
     </div>
     <div class="settings-content">
      <input type="checkbox" id="card" name="card" class="hidden checkbox1" />
      <input type="checkbox" id="pin" name="pin" class="hidden checkbox2" />
      <input type="checkbox" id="amount" name="amount" class="hidden checkbox3" />
      <input type="checkbox" id="limit" name="limit" class="hidden checkbox4" />
      <div class="new">
       <div class="newcard">
        <p>Choose a card to pay with</p>
        <input type="radio" id="card1" name="cards" class="hidden card1" checked />
          <input type="radio" id="card2" name="cards" class="hidden card2" />
          <label for="card1" class="card1l label"><span></span><p>1234-1234-1234-1234</p></label>
          <br />
          <label for="card2" class="card2l label"><span></span><p>0000-0000-0000-0000</p></label>
          <label for="card">
           <p class="confirm">Zatwierdź</p>
          </label>
       </div>
       <div class="newpin">
        <p>Enter a new PIN</p>
        <input type="password" maxlength="4" />
        <label for="pin">
         <p class="confirm">Confirm</p>
        </label>
       </div>
       <div class="newamount">
        <p>Enter amount to pay without confirmation</p>
        <div>
         <input type="number" min="1" max="10000" value="100" />
         <span>€</span>
        </div>
        <label for="amount">
         <p class="confirm">Confirm</p>
        </label>
       </div>
       <div class="newlimit">
        <p>Enter a new payment count limit</p>
        <input type="number" min="1" max="3000" value="3" />
        <label for="limit">
         <p class="confirm">Confirm</p>
        </label>
       </div>
      </div>
      <label for="card">
       <div class="set">
        <span class="ico creditcard"></span>
        <p>Choose a card to use</p>
       </div>
      </label>
      <label for="pin">
       <div class="set">
        <span class="ico pincode"></span>
        <p>Change your PIN code</p>
       </div>
      </label>
      <label for="amount">
       <div class="set">
        <span class="ico money"></span>
        <p>Amount without confirmation</p>
       </div>
      </label>
      <label for="limit">
       <div class="set">
        <span class="ico limit"></span>
        <p>Payment count limit</p>
       </div>
      </label>
     </div>
     <div class="menu">
      <label for="terminal">
       <div class="menuitem terminal">
        <div>
         <span></span>
         <p>Terminal</p>
        </div>
       </div>
      </label>
      <span class="divider"></span>
      <label for="payment">
      <div class="menuitem payment">
       <div>
        <span></span>
        <p>Payment</p>
       </div>
      </div>
      </label>
      <span class="divider"></span>
      <label for="settings">
       <div class="menuitem settings">
        <div>
         <span></span>
         <p>Settings</p>
        </div>
       </div>
      </label>
     </div>
    </div>
    <div class="navigation">
     <span class="back"></span>
     <span class="home"></span>
     <span class="opened"></span>
    </div>
   </div>
   <label for="topayment">
    <span class="logo"></class>
   </label>
  </div>
 </div>
</div>
```

```css
:root {
 --background: #79796a;
 --phone-background: #000;
 --border-background: #868695;
 --border-buttons-background: #353526;
 --camera-background: #868695;
 --camera-lens-background: #20202f;
 --detectors-light-background: #dbdbea;
 --detectors-motion-background: #d90000;
 --speaker-background: repeating-linear-gradient(45deg, rgba(255,255,255,0) 0%, rgba(255,255,255,1) 2%, rgba(255,255,255,0) 4%), repeating-linear-gradient(315deg, rgba(255,255,255,0) 0%, rgba(255,255,255,1) 2%, rgba(255,255,255,0) 4%);
 --screen-background: #004c9a;
 --logo-background: url("https://zgrajsie.com/codepen/smartphone/img/zgraj sie.jpg") center no-repeat;
 --statusbar-background: #0d203d;
 --icon1-background: url("https://zgrajsie.com/codepen/smartphone/img/cloud.svg") center no-repeat;
 --icon2-background: url("https://zgrajsie.com/codepen/smartphone/img/ipko.svg") center no-repeat;
 --icon3-background: url("https://zgrajsie.com/codepen/smartphone/img/pin.svg") center no-repeat;
 --nfc-background: url("https://zgrajsie.com/codepen/smartphone/img/nfc.svg") center no-repeat;
 --wifi-background: url("https://zgrajsie.com/codepen/smartphone/img/wifi.svg") center no-repeat;
 --coverage-background: url("https://zgrajsie.com/codepen/smartphone/img/coverage.svg") center no-repeat;
 --battery-background: url("https://zgrajsie.com/codepen/smartphone/img/battery.svg") center no-repeat;
 --application-app-keyboard-cancel-background: #ff4e37 url("https://zgrajsie.com/codepen/smartphone/img/cancel.svg") center no-repeat;
 --application-app-keyboard-undo-background: #fff404 url("https://zgrajsie.com/codepen/smartphone/img/undo.svg") center no-repeat;
 --application-app-keyboard-accept-background: #01f964 url("https://zgrajsie.com/codepen/smartphone/img/accept.svg") center no-repeat;
 --application-app-money-background: url("https://zgrajsie.com/codepen/smartphone/img/money.svg") center no-repeat;
 --application-app-settings-background: #00468c;
 --application-app-settings-creditcard-background: url("https://zgrajsie.com/codepen/smartphone/img/creditcard.svg") center no-repeat;
 --application-app-settings-pincode-background: url("https://zgrajsie.com/codepen/smartphone/img/pincode.svg") center no-repeat;
 --application-menu-background: #013789;
 --application-menu-background-active: #0059b3;
 --application-menu-terminal-background: url("https://zgrajsie.com/codepen/smartphone/img/terminal.svg") center no-repeat;
 --application-menu-payment-background: url("https://zgrajsie.com/codepen/smartphone/img/payment.svg") center no-repeat;
 --application-menu-settings-background: url("https://zgrajsie.com/codepen/smartphone/img/settings.svg") center no-repeat;
 --application-menu-divider-background: #00bfff;
 --navigation-background: #fff;
 --navigation-back-background: url("https://zgrajsie.com/codepen/smartphone/img/back.svg") center no-repeat;
 --navigation-home-background: url("https://zgrajsie.com/codepen/smartphone/img/home.svg") center no-repeat;
 --navigation-opened-background: url("https://zgrajsie.com/codepen/smartphone/img/opened.svg") center no-repeat;
}

html, body {
 margin: 0;
 padding: 0;
 background: var(--background);
  font-family: Sans-Serif;
}

.content {
 width: 100%;
 height: 99vh;
 display: flex;
 align-items: center;
 justify-content: center;
 background: var(--background);
}

.phone {
 width: 14em;
 height: 29em;
 background: var(--phone-background);
 border-radius: 2em;
 transform: scale(1.25);
}

.border {
 position: relative;
 top: -0.25em;
 left: -0.25em;
 width: inherit;
 height: inherit;
 background: inherit;
 border-radius: inherit;
 border: var(--border-background) solid .3em;
}

.volume, .volume::before {
 position: absolute;
 left: -0.25em;
 z-index: -1;
}

.volume::before {
 border-radius: 2em;
 width: .5em;
 height: 3em;
 background: var(--border-buttons-background);
}

.up::before {
 content: '';
 top: 4em;
}

.down::before {
 content: '';
 top: 8em;
}

.camera, .camera::before {
 position: absolute;
 left: 1em;
 top: .2em;
}

.camera::before {
 content: '';
 width: .8em;
 height: .8em;
 background: var(--camera-background);
 border-radius: 50%;
}

.lens, .lens::before {
 position: absolute;
}

.lens::before {
 content: '';
 top: .45em;
 left: 1.25em;
 width: .3em;
 height: .3em;
 background: var(--camera-lens-background);
 border-radius: 50%;
 z-index: 2;
 opacity: .35;
}

.detectors {
 position: absolute;
}

.light, .light::before {
 position: absolute;
}

.light::before {
 content: '';
 left: 5em;
 top: .65em;
 width: .3em;
 height: .3em;
 border-radius: 50%;
 background: var(--detectors-light-background);
 opacity: .3;
}

.motion, .motion::before {
 position: absolute;
}

.motion::before {
 content: '';
 left: 5.5em;
 top: .7em;
 width: .2em;
 height: .2em;
 border-radius: 50%;
 background: var(--detectors-motion-background);
 opacity: .3;
}

.speaker, .speaker::before {
 position: absolute;
}

.speaker::before {
 content: '';
 left: 6em;
 top: .65em;
 width: 2em;
 height: .3em;
 background: var(--speaker-background);
 border-radius: 2em;
 opacity: .3;
}

.screen {
 background: var(--screen-background);
 position: absolute;
 top: 1.5em;
 left: .5em;
 width: 13em;
 height: 26em;
 border-radius: .75em;
}

.logo {
 position: absolute;
  top: 27.75em;
 left: 6.5em;
 width: 1em;
 height: 1em;
 background: var(--logo-background);
 background-size: 1em 1em;
 border-radius: 50%;
  cursor: pointer;
}

.logo:hover {
  mix-blend-mode: screen;
}

.statusbar {
 position: absolute;
 display: flex;
 width: 100%;
 height: 1em;
 background: var(--statusbar-background);
 border-radius: .75em .75em 0 0;
}

.i1 {
 left: .5em;
 background: var(--icon1-background);
}

.i2 {
 left: 1.25em;
 background: var(--icon2-background);
}

.i3 {
 left: 2em;
 background: var(--icon3-background);
}

.procent {
 position: absolute;
 display: flex;
 align-items: center;
 right: 4.1em;
 height: 100%;
 width: 2em;
 font-size: .5em;
 font-family: "Roboto";
 font-weight: 400;
 color: #fff;
}

.nfc {
 position: absolute;
 right: 4.6em;
 background: var(--nfc-background);
 transform: scale(.9);
}

.wifi {
 position: absolute;
 right: 3.9em;
 background: var(--wifi-background);
}

.coverage {
 position: absolute;
 right: 3.2em;
 background: var(--coverage-background);
 transform: scale(.9);
}

.battery {
 position: absolute;
 right: 1.6em;
 background: var(--battery-background);
 transform: scale(1.3);
}

.time {
 position: absolute;
 display: flex;
 align-items: center;
 right: .5em;
 height: 100%;
 width: 2.5em;
 font-size: .5em;
 font-family: "Roboto";
 font-weight: 400;
 color: #fff;
}

.icon {
 position: absolute;
 width: 0.5em;
 height: 1em;
 filter: invert(100%);
 background-size: .5em .5em;
}

.application {
 margin-top: 1em;
 height: 23.5em;
 overflow: hidden;
}

.terminal-content {
 display: flex;
 flex-direction: column;
 align-items: center;
 justify-content: center;
 transform: scale(1,1);
 transform-origin: left;
 transition: transform 250ms ease-in-out;
}

.amount {
 display: block;
 margin-top: 1em;
 padding: .25em;
 background: #fff;
 text-align: right;
 width: 80%;
 border-radius: .5em;
 font-weight: 400;
}

.amount > p {
 position: absolute;
 top: .25em;
 border-radius: 1em;
 background: #e0e0e0;
 padding-left: .5em;
 padding-right: .5em;
  cursor: pointer;
  transition: background 150ms ease-in-out;
}

.amount > p:hover {
  background: #a0a0a0;
}

.keyboard {
 margin-top: 2em;
 display: flex;
 width: 80%;
 height: 16em;
 align-items: stretch;
 justify-content: space-evenly;
 font-weight: 400;
}

.keyboard > div {
 display: flex;
 flex-direction: column;
 align-items: center;
 justify-content: space-evenly;
}

.keyboard > div > p {
 display: flex;
 align-items: center;
 justify-content: center;
 width: 3em;
 height: 3em;
 margin: 0;
 border-radius: 1em;
 cursor: default;
  transition: background 100ms ease-in-out;
  cursor: pointer;
}

.keyboard > div > p:not(:last-child) {
 background: #fff;
}

.keyboard > div > p:not(:last-child):hover {
 background: #e0e0e0;
}

.cancel {
 background: var(--application-app-keyboard-cancel-background);
 background-size: 1em 1em;
}

.cancel:hover{
  background-color: #df432f;
}

.undo {
 background: var(--application-app-keyboard-undo-background);
 background-size: 1em 1em;
}

.undo:hover {
  background-color: #e0d504;
}

.accept {
 background: var(--application-app-keyboard-accept-background);
 background-size: 1em 1em;
}

.accept:hover {
  background-color: #01ce53;
}

.payment-content {
 position: relative;
 bottom: 20em;
 display: flex;
 flex-direction: column;
 align-items: center;
 justify-content: space-evenly;
 height: 20em;
 transform: scale(1,1);
 transition: transform 250ms ease-in-out;
}

.payment-content > p {
 text-align: center;
 color: #fff;
}

.to-payment-content {
 position: relative;
 bottom: 40em;
 display: flex;
 flex-direction: column;
 align-items: center;
 justify-content: space-evenly;
 height: 20em;
 transform: scale(0,0);
 transform-origin: top;
 transition: transform 100ms ease-in-out;
}

.to-payment-content > p {
 text-align: center;
 color: #fff;
}

.to-payment {
 display: flex;
 width: 80%;
 height: 3em;
 justify-content: space-evenly;
}

.reject {
 background: var(--application-app-keyboard-cancel-background);
 background-size: 1.5em 1em;
 width: 3em;
 height: 2em;
 border-radius: 2em;
  cursor: pointer;
}

.reject:hover {
  background-color: #df432f;
}

.okay {
 background: var(--application-app-keyboard-accept-background);
 background-image: url("https://zgrajsie.com/codepen/smartphone/img/okay.svg");
 background-size: 1.5em 1em;
 width: 3em;
 height: 2em;
 border-radius: 2em;
  cursor: pointer;
}

.okay:hover {
  background-color: #01ce53;
}

.no-payment {
 font-weight: 700;
}

.money {
 background: var(--application-app-money-background);
 background-size: 3em 3em;
 width: 3em;
 height: 3em;
 filter: invert(100%);
}

.settings-content {
 position: relative;
 bottom: 60em;
 display: flex;
 flex-direction: column;
 align-items: center;
 justify-content: center;
 transform: scale(1,1);
 transform-origin: right;
 transition: transform 250ms ease-in-out;
}

.settings-content > label {
 width: 100%;
}

.creditcard {
 background: var(--application-app-settings-creditcard-background);
}

.pincode {
 background: var(--application-app-settings-pincode-background);
}

.limit {
 background: var(--application-menu-payment-background);
}

.ico {
 background-size: 2em 1em;
 width: 2em;
 height: 1em;
 filter: invert(100%);
}

.set {
 display: flex;
 align-items: center;
 justify-content: flex-start;
 height: 3em;
 width: 100%;
 margin-top: .1em;
 background: var(--application-app-settings-background);
 color: #fff;
 font-size: .75em;
  transition: background 200ms ease-in-out;
  cursor: pointer;
}

.set:hover {
  background: #00378c;
}

.new {
 position: absolute;
 top: 1.5em;
 background: #e0e0e0;
 border-radius: 1em;
 width: 90%;
 height: 15em;
 z-index: 2;
 text-align: center;
 transform: scale(0,0);
 transition: transform 300ms ease-in-out;
}

.newcard {
 display: flex;
 flex-direction: column;
 align-items: center;
 justify-content: center;
 height: inherit;
}

.newcard > .label {
 transition: color 150ms ease-in-out;
}

.newcard > label > span {
 background: var(--application-app-settings-creditcard-background);
 background-size: 2em 1em;
 width: 2em;
 height: 1em;
 display: inline-block;
}

.newcard > label > p {
 font-size: .75em;
 display: inline-block;
}

.newpin {
 display: flex;
 flex-direction: column;
 align-items: center;
 justify-content: center;
 height: inherit;
}

.newpin > input {
 text-align: center;
 width: 4em;
}

.newamount {
 display: flex;
 flex-direction: column;
 align-items: center;
 justify-content: center;
 height: inherit;
}

.newamount > div > input {
 text-align: center;
 display: inline;
 width: 7em;
}

.newamount > div > span {
 text-align: center;
 display: inline;
}

.newlimit {
 display: flex;
 flex-direction: column;
 align-items: center;
 justify-content: center;
 height: inherit;
}

.newlimit > input {
 text-align: center;
 width: 5em;
}

.confirm {
 margin-top: 1em;
 font-weight: 700;
 background: #000;
 color: #fff;
 border-radius: 1em;
 box-shadow: none;
 padding: .25em 1em .25em 1em;
  cursor: pointer;
  transition: opacity 150ms ease-in-out;
}

.confirm:hover {
  opacity: .75;
}

.menu {
 position: absolute;
 bottom: 1.5em;
 width: 100%;
 height: 2.5em;
 background: var(--application-menu-background);
 display: flex;
 align-items: center;
 justify-content: space-evenly;
  font-family: Roboto;
}

.menu > label > div {
  transition: background 100ms ease-in-out;
  cursor: pointer;
}

.menu > label:hover > div {
  background: #0139b3;
}

.menuitem {
 width: 4.25em;
 height: 2.5em;
 display: flex;
 align-items: center;
 justify-content: center;
}

.divider {
 width: .05em;
 height: 80%;
 background: var(--application-menu-divider-background);
 border-radius: 3em;
 opacity: .5;
}

.menuitem > div > p {
 display: block;
 color: #fff;
 font-size: .5em;
 width: inherit;
 text-align: center;
 margin: .25em 0 0 0;
 opacity: .75;
}

.terminal > div > span {
 background: var(--application-menu-terminal-background);
}

.payment > div > span {
 background: var(--application-menu-payment-background);
}

.settings > div > span {
 background: var(--application-menu-settings-background);
}

.menuitem > div > span {
 display: block;
 width: inherit;
 height: 1.25em;
 filter: invert(100%);
 opacity: .75;
 background-size: 2em 1.25em;
}

.navigation {
 position: absolute;
 bottom: 0;
 background: var(--navigation-background);
 width: 100%;
 height: 1.5em;
 border-radius: 0 0 .75em .75em;
 display: flex;
 justify-content: space-evenly;
 opacity: .75;
}

.back {
 background: var(--navigation-back-background);
}

.home {
 background: var(--navigation-home-background);
}

.opened {
 background: var(--navigation-opened-background);
}

.navigation > span {
 width: 2em;
 background-size: .75em .75em;
}

.hidden {
 display: none;
}

.radio1:not(:checked) ~ .content > .phone > .border > .screen > .application > .terminal-content {
 transform: scale(0,1);
}

.radio1:checked ~ .content > .phone > .border > .screen > .application > .payment-content {
 transform-origin: right;
}

.radio1:checked ~ .content > .phone > .border > .screen > .application > .menu > label > .terminal {
 background: var(--application-menu-background-active);
}

.radio2:not(:checked) ~ .content > .phone > .border > .screen > .application > .payment-content {
 transform: scale(0,1);
}

.radio2:checked ~ .content > .phone > .border > .screen > .application > .menu > label >  .payment {
 background: var(--application-menu-background-active);
}

.radio3:not(:checked) ~ .content > .phone > .border > .screen > .application > .settings-content {
 transform: scale(0,1);
}

.radio3:checked ~ .content > .phone > .border > .screen > .application > .payment-content {
 transform-origin: left;
}

.radio3:checked ~ .content > .phone > .border > .screen > .application > .menu > label >  .settings {
 background: var(--application-menu-background-active);
}

.radio4:checked ~ .content > .phone > .border > .screen > .application > .to-payment-content {
 transform: scale(1,1);
 transition: transform 250ms ease-in-out;
}

.radio4:checked ~ .content > .phone > .border > .screen > .application > .menu > label >  .payment {
 background: var(--application-menu-background-active);
}

.checkbox1:not(:checked) ~ .new > .newcard {
 display: none;
}

.checkbox2:not(:checked) ~ .new > .newpin {
 display: none;
}

.checkbox3:not(:checked) ~ .new > .newamount {
 display: none;
}

.checkbox4:not(:checked) ~ .new > .newlimit {
 display: none;
}

.checkbox1:checked ~ .new, .checkbox2:checked ~ .new, .checkbox3:checked ~ .new, .checkbox4:checked ~ .new {
 transform: scale(1,1);
}

@media screen and (max-width: 500px) {
  .phone {
    transform: scale(.6);
  }
}

.card1:checked ~ .card1l, .card2:checked ~ .card2l {
 color: #ff0000;
}
```

---
theme: default
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
drawings:
  persist: false
title: Clean Code & Code Smells
layout: intro
download: true
---

# Clean Code and Code Smells


---

<img class="w-[280px] top-1/5 absolute right-16" src="https://assets.codegrip.tech/wp-content/uploads/2019/08/09093304/1-Code-Smell.jpg" />

<div class="w-full">

  <h1 class="font-bold text-left leading-3">
	<span class="text-blue-300">Clean Code</span> &
	<span class="text-red-300">Code Smells</span>
  </h1>


  <div class="text-left text-gray-400 mt-12">

  - What are these?

  - Why we must care about them?

  - Solutions to achieve better code?

  - Showcases

  </div>

</div>


---

<h1 class="text-center mt-40">What do you think about "Clean Code and Code Smells"?</h1>
<p class="text-center">What are these?</p>


---

<h1 class="font-bold pb-2 leading-loose pb-8 block">Examples of missing <span className="text-blue-300 ">Clean Code</span> and
<span className="text-red-300 ">Code Smells</span> bad?</h1>


- Long methods
- Long parameeter list
- Large class
- Duplication
- Variables name
- count of files and directories
- ..


<style>
  li {
  	@apply text-gray-400 !important;
  }
</style>

<div class="absolute right-16 top-38 overflow-auto max-h-[360px] max-w-[500px]">

```tsx {0|1-3|4-43}
function calculate (id, baseProfit, raise, rate,
  days, hours, offDays, offHours, loan, insurance,
  absences, holidays){

  if(x){
  	const sit = ipsum == null ? 0 : ipsum.sit;
  	dolor = sit - amet(dolor);
  	return sit ? consectetur(ipsum, 0, dolor < 0 ? 0 : dolor) : [];
  }

  if (!elit.sit) {
    return [];
  }

  const sed = elit[0];
  const data = eiusmod.tempor(sed) ? sed : [sed];

  ut = labore.et(amet(ut), 0);
  const sit = ipsum == null ? 0 : ipsum.sit;

  if (!sit || ut < 1) {
    return [];
  }

  let dolore = 0;
  let magna = 0;
  const aliqua = new eiusmod(labore.ut(sit / ut));

  while (dolore < sit) {
    aliqua[magna++] = consectetur(ipsum, dolore, (dolore += ut));
  }
   if(x){
  	const sit = ipsum == null ? 0 : ipsum.sit;
  	dolor = sit - amet(dolor);
  	return sit ? consectetur(ipsum, 0, dolor < 0 ? 0 : dolor) : [];
  }

  if (!elit.sit) {
    return [];
  }

  const sed = elit[0];
  const data = eiusmod.tempor(sed) ? sed : [sed];

}

```
</div>


---

<h1 class="top-56 absolute left-40">
Why we should care about clean code?
</h1>


---

# Why we must care?

- Short memorry issue
- Readability
- Extensibility
- Extendibility
- Understanding quickly
- Your ideas...

<img class="absolute right-16 max-w-[300px] top-30" src="https://townsquare.media/site/151/files/2016/01/2016-01-20_0948.png%3Fw=980&q=75" />

<style>
  li {
  	@apply text-gray-400 !important;
  }
</style>


---

# Project Management Triangle

<img src="https://i0.wp.com/garywoodfine.com/wp-content/uploads/2018/09/quality-triangle-1-2039663718-1537862502348.jpg?w=697&ssl=1" class="mx-auto max-w-[390px] mt-16 block" />


---

<h1 class="top-50 absolute w-full text-center left-0">
Solutions to code smells?
</h1>


---

<img src="https://unsplash.com/photos/7oBmQz4bfrQ/download?ixid=MnwxMjA3fDB8MXxzZWFyY2h8NXx8d2ViJTIwcHJvZ3JhbW1pbmd8ZW58MHwxfHx8MTY1MjMzMTcyMw&force=true&w=640"
class="absolute object-fit max-w-[300px] right-14 top-16" />
<img class="max-w-[120px] absolute top-[320px] right-[330px]" src="https://gcdnb.pbrd.co/images/PCiM4TMyjWRI.png?o=1" />
<img class="max-w-[120px] absolute top-[130px] right-[300px]" src="https://gcdnb.pbrd.co/images/CvxMpQRa5483.png?o=1" />

# Solutions to code smells

- Eslint/Prettier
- Sonar cube
- Husky
- EditorConfig
- GitHub integrations (Codecov / CodeFactor)
- Your Ideas


<style>
  li {
  	@apply text-gray-400 !important;
  }
</style>


---

# Showcases


<h4 class="text-red-500 mb-2 mt-8">❌ Bad</h4>

```ts
var d; // elapsed time in days
```
<v-click>
<h4 class="text-red-500 my-2 mt-4">✅ Good</h4>

```ts
var elapsedDays; // elapsed time in days
```

</v-click>


  <v-click>
  <h4 class="text-red-500 mb-2 mt-16">❌ Bad</h4>

  ```ts
 const yyyymmdstr = moment().format("YYYY/MM/DD");
  ```
  </v-click>
  <v-click>
  <h4 class="text-red-500 my-2 mt-4">✅ Good</h4>

  ```ts
const currentDate = moment().format("YYYY/MM/DD");
  ```

  </v-click>



---

# Showcases


<h4 class="text-red-500 mb-2 mt-8">❌ Bad</h4>

```ts
if (student.classes.length < 7) {
   // Do something
}
```
<v-click>
<h4 class="text-red-500 my-2 mt-4">✅ Good</h4>

```ts
if (student.classes.length < MAX_CLASSES_PER_STUDENT) {
    // Do something
}
```

</v-click>


---

# Showcases


<h4 class="text-red-500 mb-2 mt-8">❌ Bad</h4>

```ts
function book(aCustomer, boolean isPremium) {
  if(isPremium)
    // logic for premium book right here
  else
    // logic for regular booking right here
}

```
<v-click>
<h4 class="text-red-500 my-2 mt-4">✅ Good</h4>

```ts
function book(aCustomer, boolean isPremium) {
  if(isPremium)
    premiumBook(aCustomer)
  else
    regularBook(aCustomer)
}
```

</v-click>


---

# Showcases


<h4 class="text-red-500 mb-2 mt-8">❌ Bad</h4>

```ts
const Car = {
  carMake: "Honda",
  carModel: "Accord",
  carColor: "Blue"
};

function paintCar(car, color) {
  car.carColor = color;
}
```
<v-click>
<h4 class="text-red-500 my-2 mt-4">✅ Good</h4>

```ts
const Car = {
  make: "Honda",
  model: "Accord",
  color: "Blue"
};

function paintCar(car, color) {
  car.color = color;
}
```

</v-click>


---

# Showcases


<h4 class="text-red-500 mb-2 mt-8">❌ Bad</h4>

```ts
if (foo) {
  doSomething();
}
```
<v-click>
<h4 class="text-red-500 my-2 mt-4">✅ Good</h4>

```ts
foo && doSomething();
```

</v-click>


---

# Showcases

<h4 class="text-red-500 mb-2 mt-8">❌ Bad</h4>

```ts
function emailClients(clients) {
  clients.forEach(client => {
    const clientRecord = database.lookup(client);
    if (clientRecord.isActive()) {
      email(client);
    }
  });
}
```
<v-click>
<h4 class="text-red-500 my-2 mt-4">✅ Good</h4>

```ts
function emailActiveClients(clients) {
  clients.filter(isActiveClient).forEach(email);
}

function isActiveClient(client) {
  const clientRecord = database.lookup(client);
  return clientRecord.isActive();
}
```

</v-click>


---


# Showcases

<h4 class="text-red-500 mb-2 mt-8">❌ Bad</h4>

<div class="overflow-auto max-h-[380px]">

```ts
function parseBetterJSAlternative(code) {
  const REGEXES = [
    // ...
  ];

  const statements = code.split(" ");
  const tokens = [];
  REGEXES.forEach(REGEX => {
    statements.forEach(statement => {
      // ...
    });
  });

  const ast = [];
  tokens.forEach(token => {
    // lex...
  });

  ast.forEach(node => {
    // parse...
  });
}
```

</div>

---

# Showcase

<h4 class="text-red-500 my-2 mt-8">✅ Good</h4>

<div class="overflow-auto max-h-[380px]">

```ts
function parseBetterJSAlternative(code) {
  const tokens = tokenize(code);
  const syntaxTree = parse(tokens);
  syntaxTree.forEach(node => {
    // parse...
  });
}

function tokenize(code) {
  const REGEXES = [
    // ...
  ];

  const statements = code.split(" ");
  const tokens = [];
  REGEXES.forEach(REGEX => {
    statements.forEach(statement => {
      tokens.push(/* ... */);
    });
  });

  return tokens;
}

function parse(tokens) {
  const syntaxTree = [];
  tokens.forEach(token => {
    syntaxTree.push(/* ... */);
  });

  return syntaxTree;
}
```

</div>


---

# Thank you so much


<span class="text-gray-400 absolute left-16 bottom-8">Nariman Movaffaghi from LMS team with ❤️</span>
<span class="text-gray-400 absolute right-16 bottom-8 text-sm">Made with <a href="https://sli.dev">Sli.dev</a></span>

<style>
	a:hover{
		color: lightblue;
	}
</style>

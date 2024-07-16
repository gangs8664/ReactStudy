# JS Syntax [ import, export ]

<aside>
🗣 React 프로젝트에, 실제로 모든 최신의 JavaScript에서 `모듈` 이라 불리는 여러 자바스크립트 파일들에 코드를 분리한다.

`모듈` : 자바스크립트 `파일` (⇒ .js)

이렇게 `분리하여 관리`하면 각 파일 또는 모듈의 `목적을 명확하게` 하고 `관리가 용이`하다는 장점이 있다.

w3schools) This makes it `easier to maintain` a code-base : 이렇게 하면 코드베이스를 더 쉽게 유지 관리할 수 있습니다.
`코드베이스` : 소스 코드의 모음

```jsx
//Modules also rely on type="module" in the <script> tag.

<script type="module">
import message from "./message.js";
</script>
```

import, export 하는 방법 총정리

</aside>

다른 파일의 기능에 계속 액세스하려면 export, import statement가 필요하다.

### 1) export

두 가지 유형의 export 가 존재한다.

### 1-1) named export

- `named` ⇒ `export` `const` `someData` = `…`;
    - `Named exports`는 `이름으로 import`되어야한다.
    - ⇒ `import` `{ someData }` `from` `‘./path/to/file.js’;`
    - named exports를 import할 때, 아래 구문을 이용해 `한 번에 모든` named exports를 import할 수 있다.
    - ⇒ `import` `*` `as` `upToYou` `from` `‘./path/to/file.js’;`
    - `upToYou`는 모든 exported `변수/함수`를 **`하나의 자바스크립트 객체에` 모은다.**
        - ex) export const someData = …(/path/to/file.js)
        - upToYou.someData로 upToYou에 액세스 할 수 있다.

### 1-2) default export

- `default` ⇒ `export` `default` `…`;
    - `import` `someNameOfYourChoice` `from` `‘./path/to/file.js’;`
    - 왜 someNameOfYourChoice냐? : 전적으로 코드 작성자에게 달려있다는 뜻이다. 뭘하던지!
    

<aside>
🗣 파일 하나는 `오직 하나의 default export`와 `무한한 named exports`를 가질 수 있다.
`하나의 default`를 `같은 파일 내`에서 `named exports와 믹스`할 수 있다.

</aside>
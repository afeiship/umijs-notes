# dynamic-import
- https://umijs.org/zh-CN/docs/load-on-demand#%E5%90%AF%E7%94%A8%E6%8C%89%E9%9C%80%E5%8A%A0%E8%BD%BD

```js
import { dynamic } from 'umi';

const delay = (timeout) => new Promise(resolve => setTimeout(resolve, timeout));

const App = dynamic({
  loader: async function() {
    await delay(/* 1s */1000);
    return () => <div>I will render after 1s</div>;
  },
});
```

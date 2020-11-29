# simple-webworker

## 介绍
基于 simple-web-worker，方便再webpack打包的项目中使用web worker，根据线程数量维护worker任务队列
> push方法将任务添加至任务队列，调用simple-web-worker的run方法实现webwoker并在完成时自动销毁
## 使用
```js
// INIT 
const worker =  new WorkerQueue();
worker.push(fn,callback[, ...[, argument]]]);
```
### 参数
1. fn:  
   为web worker 执行的耗时操作function，需要注意不能传递postMessage不支持的数据类型
2. callback:  
   为执行完成后的回调
3. argument:  
   传递的参数
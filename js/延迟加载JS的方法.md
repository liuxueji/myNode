延迟加载JS方法：async、defer



- 如果不使用JS延迟加载，那么就会按顺序执行，遇到script标签就会等待 js下载、js解析，下载解析完了，才会继续执行

-----------------------------js下载 js解析----------------------------------，---表示页面渲染

所以，如果不使用JS延迟加载，那么script标签就不要放在头部，要放在body底部，</body 之前，这样才不会阻塞页面渲染，导致白屏



- async，它表示js解析与dom渲染同步执行。它不是按顺序执行的，如果引入a.js、b.js，那么可能先执行b，也有可能先执行a。基于这个原因，在async一定不能有依赖关系，例如a依赖b，可能b还没加载a就加载了，导致a无法正常使用
- defer，它表示dom渲染完后再执行js解析，原理就类似将script写到body底部。defer会按顺序执行js，可以有依赖关系。



还有其他方法：动态创建DOM方式、使用jq的getScript()、使用setTimeout。
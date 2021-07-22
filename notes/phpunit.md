some functions for phpunit:
```
$app：Laravel 5.1 应用实例
$code：Artisan命令返回的最后一个码值
refreshApplication()：刷新应用。该操作由TestCase的setup()方法自动调用
call($method, $uri, $parameters = [], $cookies = [], $files = [], $server = [], $content = null)：调用给定URI并返回响应
callSecure($method, $uri, $parameters = [], $cookies = [], $files = [], $server = [], $content = null)：调用给定HTTPS URI并返回响应
action($method, $action, $wildcards = [], $parameters = [], $cookies = [], $files = [], $server = [], $content = null)：调用控制器动作并返回响应
route($method, $name, $routeParameters = [], $parameters = [], $cookies = [], $files = [], $server = [], $content = null)：调用命名路由并返回响应
instance($abstract, $object)：在容器中注册对象实例
expectsEvents($events)：指定被给定操作触发的事件列表
withoutEvents()：无需触发事件模拟事件调度
expectsJobs($jobs)：为特定操作执行被调度的任务列表
withSession(array $data)：设置session到给定数组
flushSession()：清空当前session中的内容
startSession()：开启应用Session
actingAs($user)：为应用设置当前登录用户
be($user)：为应用设置当前登录用户
seeInDatabase($table, array $data, $connection = null)：断言给定where条件在数据库中存在
notSeeInDatabase($table, $array $data, $connection = null)：断言给定where条件在数据库中不存在
missingFromDatabase($table, array $data, $connection = null)：notSeeInDatabase()的别名
seed()：填充数据库
artisan($command, $parameters = [])：执行Artisan命令并返回码值
```

PHPUnit 的断言方法
```
assertPageLoaded($uri, $message = null)：断言最后被加载的页面；如果加载失败抛出异常：$uri/$message
assertResponseOk()：断言客户端返回的响应状态码是否是200
assertReponseStatus($code)：断言客户端返回的响应状态码是否和给定码值相匹配
assertViewHas($key, $value = null)：断言响应视图包含给定数据片段
assertViewHasAll($bindings)：断言视图包含给定数据列表
assertViewMissing($key)：断言响应视图不包含给定数据片段
assertRedirectedTo($uri, $with = [])：断言客户端是否重定向到给定URI
assertRedirectedToRoute($name, $parameters = [], $with = [])：断言客户端是否重定向到给定路由
assertRedirectedToAction($name, $parameters = [], $with = [])：断言客户端是否重定向到给定动作
assertSessionHas($key, $value = null)：断言session包含给定键/值
assertSessionHasAll($bindings)：断言session包含给定值列表
assertSessionHasErrors($bindings = [])：断言session包含绑定错误
assertHasOldInput()：断言session中包含上一次输入
```
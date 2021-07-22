some functions for crawler:
```
$this->response: web application return the last one response.
$this->currentUri: current visit url.
visit($uri): visit the uri by get request.
get($uri, array $headers = []):get the uri page content by get request, it can deliver request header info(optional) 
post($uri, array $data = [], array $headers = [])：submit a post request to the given uri
put($uri, array $data = [], array $headers = [])：提交PUT请求到给定URI
patch($uri, array $data = [], array $headers = [])：提交PATCH请求到给定URI
delete($uri, array $data = [], array $headers = [])：提交DELETE请求到给定URI
followRedirects()：根据最后响应进行任意重定向
see($text, $negate = false)：断言给定文本在页面中是否出现
seeJson(array $data = null)：断言响应中是否包含JSON，如果传递了$data，还要断言包含的JSON是否与给定的匹配
seeStatusCode($status)：断言响应是否包含期望的状态码
seePageIs($uri)：断言当前页面是否与给定URI匹配
seeOnPage($uri)和landOn($uri)：seePageIs()的别名
click($name)：使用给定body、name或者id点击链接
type($text, $element)：使用给定文本填充输入框
check($element)：检查页面上的checkbox复选框
select($option, $element)：选择页面上下拉列表的某个选项
attach($absolutePath, $element)：上传文件到表单
press($buttonText)：通过使用给定文本的按钮提交表单
withoutMiddleware()：在测试中不使用中间件
dump()：输出最后一个响应返回的内容
```
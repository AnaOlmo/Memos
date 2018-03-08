---


---

<h2 id="installing">Installing</h2>
<p>Using npm:</p>
<p>$ npm install axios</p>
<p>Using bower:</p>
<p>$ bower install axios</p>
<p>Using cdn:</p>

<h2 id="example"><a href="https://github.com/axios/axios#example"></a>Example</h2>
<p>Performing a  <code>GET</code>  request</p>
<p>// Make a request for a user with a given ID<br>
axios.get(’/user?ID=12345’)<br>
.then(function (response) {<br>
console.log(response);<br>
})<br>
.catch(function (error) {<br>
console.log(error);<br>
});</p>
<p>// Optionally the request above could also be done as<br>
axios.get(’/user’, {<br>
params: {<br>
ID: 12345<br>
}<br>
})<br>
.then(function (response) {<br>
console.log(response);<br>
})<br>
.catch(function (error) {<br>
console.log(error);<br>
});</p>
<p>// Want to use async/await? Add the `async` keyword to your outer function/method.<br>
async function getUser() {<br>
try {<br>
const response = await axios.get(’/user?ID=12345’);<br>
console.log(response);<br>
} catch (error) {<br>
console.error(error);<br>
}<br>
}</p>
<blockquote>
<p><strong>NOTE:</strong>  <code>async/await</code>  is part of ECMAScript 2017 and is not supported in Internet Explorer and older browsers, so use with caution.</p>
</blockquote>
<p>Performing a  <code>POST</code>  request</p>
<p>axios.post(’/user’, {<br>
firstName: ‘Fred’,<br>
lastName: ‘Flintstone’<br>
})<br>
.then(function (response) {<br>
console.log(response);<br>
})<br>
.catch(function (error) {<br>
console.log(error);<br>
});</p>
<p>Performing multiple concurrent requests</p>
<p>function getUserAccount() {<br>
return axios.get(’/user/12345’);<br>
}</p>
<p>function getUserPermissions() {<br>
return axios.get(’/user/12345/permissions’);<br>
}</p>
<p>axios.all([getUserAccount(), getUserPermissions()])<br>
.then(axios.spread(function (acct, perms) {<br>
// Both requests are now complete<br>
}));</p>
<h2 id="axios-api"><a href="https://github.com/axios/axios#axios-api"></a>axios API</h2>
<p>Requests can be made by passing the relevant config to  <code>axios</code>.</p>
<h5 id="axiosconfig"><a href="https://github.com/axios/axios#axiosconfig"></a>axios(config)</h5>
<p>// Send a POST request<br>
axios({<br>
method: ‘post’,<br>
url: ‘/user/12345’,<br>
data: {<br>
firstName: ‘Fred’,<br>
lastName: ‘Flintstone’<br>
}<br>
});</p>
<p>// GET request for remote image<br>
axios({<br>
method:‘get’,<br>
url:‘<a href="http://bit.ly/2mTM3nY">http://bit.ly/2mTM3nY</a>’,<br>
responseType:‘stream’<br>
})<br>
.then(function(response) {<br>
response.data.pipe(fs.createWriteStream(‘ada_lovelace.jpg’))<br>
});</p>
<h5 id="axiosurl-config"><a href="https://github.com/axios/axios#axiosurl-config"></a>axios(url[, config])</h5>
<p>// Send a GET request (default method)<br>
axios(’/user/12345’);</p>
<h3 id="request-method-aliases"><a href="https://github.com/axios/axios#request-method-aliases"></a>Request method aliases</h3>
<p>For convenience aliases have been provided for all supported request methods.</p>
<h5 id="axios.requestconfig"><a href="https://github.com/axios/axios#axiosrequestconfig"></a>axios.request(config)</h5>
<h5 id="axios.geturl-config"><a href="https://github.com/axios/axios#axiosgeturl-config"></a>axios.get(url[, config])</h5>
<h5 id="axios.deleteurl-config"><a href="https://github.com/axios/axios#axiosdeleteurl-config"></a>axios.delete(url[, config])</h5>
<h5 id="axios.headurl-config"><a href="https://github.com/axios/axios#axiosheadurl-config"></a>axios.head(url[, config])</h5>
<h5 id="axios.optionsurl-config"><a href="https://github.com/axios/axios#axiosoptionsurl-config"></a>axios.options(url[, config])</h5>
<h5 id="axios.posturl-data-config"><a href="https://github.com/axios/axios#axiosposturl-data-config"></a>axios.post(url[, data[, config]])</h5>
<h5 id="axios.puturl-data-config"><a href="https://github.com/axios/axios#axiosputurl-data-config"></a>axios.put(url[, data[, config]])</h5>
<h5 id="axios.patchurl-data-config"><a href="https://github.com/axios/axios#axiospatchurl-data-config"></a>axios.patch(url[, data[, config]])</h5>
<h6 id="note"><a href="https://github.com/axios/axios#note"></a>NOTE</h6>
<p>When using the alias methods  <code>url</code>,  <code>method</code>, and  <code>data</code>  properties don’t need to be specified in config.</p>
<h3 id="concurrency"><a href="https://github.com/axios/axios#concurrency"></a>Concurrency</h3>
<p>Helper functions for dealing with concurrent requests.</p>
<h5 id="axios.alliterable"><a href="https://github.com/axios/axios#axiosalliterable"></a>axios.all(iterable)</h5>
<h5 id="axios.spreadcallback"><a href="https://github.com/axios/axios#axiosspreadcallback"></a>axios.spread(callback)</h5>
<h3 id="creating-an-instance"><a href="https://github.com/axios/axios#creating-an-instance"></a>Creating an instance</h3>
<p>You can create a new instance of axios with a custom config.</p>
<h5 id="axios.createconfig"><a href="https://github.com/axios/axios#axioscreateconfig"></a>axios.create([config])</h5>
<p>var instance = axios.create({<br>
baseURL: ‘<a href="https://some-domain.com/api/">https://some-domain.com/api/</a>’,<br>
timeout: 1000,<br>
headers: {‘X-Custom-Header’: ‘foobar’}<br>
});</p>
<h3 id="instance-methods"><a href="https://github.com/axios/axios#instance-methods"></a>Instance methods</h3>
<p>The available instance methods are listed below. The specified config will be merged with the instance config.</p>
<h5 id="axiosrequestconfig"><a href="https://github.com/axios/axios#axiosrequestconfig-1"></a>axios#request(config)</h5>
<h5 id="axiosgeturl-config"><a href="https://github.com/axios/axios#axiosgeturl-config-1"></a>axios#get(url[, config])</h5>
<h5 id="axiosdeleteurl-config"><a href="https://github.com/axios/axios#axiosdeleteurl-config-1"></a>axios#delete(url[, config])</h5>
<h5 id="axiosheadurl-config"><a href="https://github.com/axios/axios#axiosheadurl-config-1"></a>axios#head(url[, config])</h5>
<h5 id="axiosoptionsurl-config"><a href="https://github.com/axios/axios#axiosoptionsurl-config-1"></a>axios#options(url[, config])</h5>
<h5 id="axiosposturl-data-config"><a href="https://github.com/axios/axios#axiosposturl-data-config-1"></a>axios#post(url[, data[, config]])</h5>
<h5 id="axiosputurl-data-config"><a href="https://github.com/axios/axios#axiosputurl-data-config-1"></a>axios#put(url[, data[, config]])</h5>
<h5 id="axiospatchurl-data-config"><a href="https://github.com/axios/axios#axiospatchurl-data-config-1"></a>axios#patch(url[, data[, config]])</h5>
<h2 id="request-config"><a href="https://github.com/axios/axios#request-config"></a>Request Config</h2>
<p>These are the available config options for making requests. Only the  <code>url</code>  is required. Requests will default to  <code>GET</code>  if  <code>method</code>is not specified.</p>
<p>{<br>
// `url` is the server URL that will be used for the request<br>
url: ‘/user’,</p>
<p>// `method` is the request method to be used when making the request<br>
method: ‘get’, // default</p>
<p>// `baseURL` will be prepended to `url` unless `url` is absolute.<br>
// It can be convenient to set `baseURL` for an instance of axios to pass relative URLs<br>
// to methods of that instance.<br>
baseURL: ‘<a href="https://some-domain.com/api/">https://some-domain.com/api/</a>’,</p>
<p>// `transformRequest` allows changes to the request data before it is sent to the server<br>
// This is only applicable for request methods ‘PUT’, ‘POST’, and ‘PATCH’<br>
// The last function in the array must return a string or an instance of Buffer, ArrayBuffer,<br>
// FormData or Stream<br>
// You may modify the headers object.<br>
transformRequest: [function (data, headers) {<br>
// Do whatever you want to transform the data</p>
<pre><code>return data;
</code></pre>
<p>}],</p>
<p>// `transformResponse` allows changes to the response data to be made before<br>
// it is passed to then/catch<br>
transformResponse: [function (data) {<br>
// Do whatever you want to transform the data</p>
<pre><code>return data;
</code></pre>
<p>}],</p>
<p>// `headers` are custom headers to be sent<br>
headers: {‘X-Requested-With’: ‘XMLHttpRequest’},</p>
<p>// `params` are the URL parameters to be sent with the request<br>
// Must be a plain object or a URLSearchParams object<br>
params: {<br>
ID: 12345<br>
},</p>
<p>// `paramsSerializer` is an optional function in charge of serializing `params`<br>
// (e.g. <a href="https://www.npmjs.com/package/qs">https://www.npmjs.com/package/qs</a>, <a href="http://api.jquery.com/jquery.param/">http://api.jquery.com/jquery.param/</a>)<br>
paramsSerializer: function(params) {<br>
return Qs.stringify(params, {arrayFormat: ‘brackets’})<br>
},</p>
<p>// `data` is the data to be sent as the request body<br>
// Only applicable for request methods ‘PUT’, ‘POST’, and ‘PATCH’<br>
// When no `transformRequest` is set, must be of one of the following types:<br>
// - string, plain object, ArrayBuffer, ArrayBufferView, URLSearchParams<br>
// - Browser only: FormData, File, Blob<br>
// - Node only: Stream, Buffer<br>
data: {<br>
firstName: ‘Fred’<br>
},</p>
<p>// `timeout` specifies the number of milliseconds before the request times out.<br>
// If the request takes longer than `timeout`, the request will be aborted.<br>
timeout: 1000,</p>
<p>// `withCredentials` indicates whether or not cross-site Access-Control requests<br>
// should be made using credentials<br>
withCredentials: false, // default</p>
<p>// `adapter` allows custom handling of requests which makes testing easier.<br>
// Return a promise and supply a valid response (see lib/adapters/README.md).<br>
adapter: function (config) {<br>
/* … */<br>
},</p>
<p>// `auth` indicates that HTTP Basic auth should be used, and supplies credentials.<br>
// This will set an `Authorization` header, overwriting any existing<br>
// `Authorization` custom headers you have set using `headers`.<br>
auth: {<br>
username: ‘janedoe’,<br>
password: ‘s00pers3cret’<br>
},</p>
<p>// `responseType` indicates the type of data that the server will respond with<br>
// options are ‘arraybuffer’, ‘blob’, ‘document’, ‘json’, ‘text’, 'stream’<br>
responseType: ‘json’, // default</p>
<p>// `xsrfCookieName` is the name of the cookie to use as a value for xsrf token<br>
xsrfCookieName: ‘XSRF-TOKEN’, // default</p>
<p>// `xsrfHeaderName` is the name of the http header that carries the xsrf token value<br>
xsrfHeaderName: ‘X-XSRF-TOKEN’, // default</p>
<p>// `onUploadProgress` allows handling of progress events for uploads<br>
onUploadProgress: function (progressEvent) {<br>
// Do whatever you want with the native progress event<br>
},</p>
<p>// `onDownloadProgress` allows handling of progress events for downloads<br>
onDownloadProgress: function (progressEvent) {<br>
// Do whatever you want with the native progress event<br>
},</p>
<p>// `maxContentLength` defines the max size of the http response content allowed<br>
maxContentLength: 2000,</p>
<p>// `validateStatus` defines whether to resolve or reject the promise for a given<br>
// HTTP response status code. If `validateStatus` returns `true` (or is set to `null`<br>
// or `undefined`), the promise will be resolved; otherwise, the promise will be<br>
// rejected.<br>
validateStatus: function (status) {<br>
return status &gt;= 200 &amp;&amp; status &lt; 300; // default<br>
},</p>
<p>// `maxRedirects` defines the maximum number of redirects to follow in node.js.<br>
// If set to 0, no redirects will be followed.<br>
maxRedirects: 5, // default</p>
<p>// `socketPath` defines a UNIX Socket to be used in node.js.<br>
// e.g. ‘/var/run/docker.sock’ to send requests to the docker daemon.<br>
// Only either `socketPath` or `proxy` can be specified.<br>
// If both are specified, `socketPath` is used.<br>
socketPath: null, // default</p>
<p>// `httpAgent` and `httpsAgent` define a custom agent to be used when performing http<br>
// and https requests, respectively, in node.js. This allows options to be added like<br>
// `keepAlive` that are not enabled by default.<br>
httpAgent: new http.Agent({ keepAlive: true }),<br>
httpsAgent: new https.Agent({ keepAlive: true }),</p>
<p>// ‘proxy’ defines the hostname and port of the proxy server<br>
// Use `false` to disable proxies, ignoring environment variables.<br>
// `auth` indicates that HTTP Basic auth should be used to connect to the proxy, and<br>
// supplies credentials.<br>
// This will set an `Proxy-Authorization` header, overwriting any existing<br>
// `Proxy-Authorization` custom headers you have set using `headers`.<br>
proxy: {<br>
host: ‘127.0.0.1’,<br>
port: 9000,<br>
auth: {<br>
username: ‘mikeymike’,<br>
password: ‘rapunz3l’<br>
}<br>
},</p>
<p>// `cancelToken` specifies a cancel token that can be used to cancel the request<br>
// (see Cancellation section below for details)<br>
cancelToken: new CancelToken(function (cancel) {<br>
})<br>
}</p>
<h2 id="response-schema"><a href="https://github.com/axios/axios#response-schema"></a>Response Schema</h2>
<p>The response for a request contains the following information.</p>
<p>{<br>
// `data` is the response that was provided by the server<br>
data: {},</p>
<p>// `status` is the HTTP status code from the server response<br>
status: 200,</p>
<p>// `statusText` is the HTTP status message from the server response<br>
statusText: ‘OK’,</p>
<p>// `headers` the headers that the server responded with<br>
// All header names are lower cased<br>
headers: {},</p>
<p>// `config` is the config that was provided to `axios` for the request<br>
config: {},</p>
<p>// `request` is the request that generated this response<br>
// It is the last ClientRequest instance in node.js (in redirects)<br>
// and an XMLHttpRequest instance the browser<br>
request: {}<br>
}</p>
<p>When using  <code>then</code>, you will receive the response as follows:</p>
<p>axios.get(’/user/12345’)<br>
.then(function(response) {<br>
console.log(response.data);<br>
console.log(response.status);<br>
console.log(response.statusText);<br>
console.log(response.headers);<br>
console.log(response.config);<br>
});</p>
<p>When using  <code>catch</code>, or passing a  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/then">rejection callback</a>  as second parameter of  <code>then</code>, the response will be available through the  <code>error</code>  object as explained in the  <a href="https://github.com/axios/axios#handling-errors">Handling Errors</a>  section.</p>
<h2 id="config-defaults"><a href="https://github.com/axios/axios#config-defaults"></a>Config Defaults</h2>
<p>You can specify config defaults that will be applied to every request.</p>
<h3 id="global-axios-defaults"><a href="https://github.com/axios/axios#global-axios-defaults"></a>Global axios defaults</h3>
<p>axios.defaults.baseURL = ‘<a href="https://api.example.com">https://api.example.com</a>’;<br>
axios.defaults.headers.common[‘Authorization’] = AUTH_TOKEN;<br>
axios.defaults.headers.post[‘Content-Type’] = ‘application/x-www-form-urlencoded’;</p>
<h3 id="custom-instance-defaults"><a href="https://github.com/axios/axios#custom-instance-defaults"></a>Custom instance defaults</h3>
<p>// Set config defaults when creating the instance<br>
var instance = axios.create({<br>
baseURL: ‘<a href="https://api.example.com">https://api.example.com</a>’<br>
});</p>
<p>// Alter defaults after instance has been created<br>
instance.defaults.headers.common[‘Authorization’] = AUTH_TOKEN;</p>
<h3 id="config-order-of-precedence"><a href="https://github.com/axios/axios#config-order-of-precedence"></a>Config order of precedence</h3>
<p>Config will be merged with an order of precedence. The order is library defaults found in  <a href="https://github.com/axios/axios/blob/master/lib/defaults.js#L28">lib/defaults.js</a>, then  <code>defaults</code>property of the instance, and finally  <code>config</code>  argument for the request. The latter will take precedence over the former. Here’s an example.</p>
<p>// Create an instance using the config defaults provided by the library<br>
// At this point the timeout config value is `0` as is the default for the library<br>
var instance = axios.create();</p>
<p>// Override timeout default for the library<br>
// Now all requests will wait 2.5 seconds before timing out<br>
instance.defaults.timeout = 2500;</p>
<p>// Override timeout for this request as it’s known to take a long time<br>
instance.get(’/longRequest’, {<br>
timeout: 5000<br>
});</p>
<h2 id="interceptors"><a href="https://github.com/axios/axios#interceptors"></a>Interceptors</h2>
<p>You can intercept requests or responses before they are handled by  <code>then</code>  or  <code>catch</code>.</p>
<p>// Add a request interceptor<br>
axios.interceptors.request.use(function (config) {<br>
// Do something before request is sent<br>
return config;<br>
}, function (error) {<br>
// Do something with request error<br>
return Promise.reject(error);<br>
});</p>
<p>// Add a response interceptor<br>
axios.interceptors.response.use(function (response) {<br>
// Do something with response data<br>
return response;<br>
}, function (error) {<br>
// Do something with response error<br>
return Promise.reject(error);<br>
});</p>
<p>If you may need to remove an interceptor later you can.</p>
<p>var myInterceptor = axios.interceptors.request.use(function () {/<em>…</em>/});<br>
axios.interceptors.request.eject(myInterceptor);</p>
<p>You can add interceptors to a custom instance of axios.</p>
<p>var instance = axios.create();<br>
instance.interceptors.request.use(function () {/<em>…</em>/});</p>
<h2 id="handling-errors"><a href="https://github.com/axios/axios#handling-errors"></a>Handling Errors</h2>
<p>axios.get(’/user/12345’)<br>
.catch(function (error) {<br>
if (error.response) {<br>
// The request was made and the server responded with a status code<br>
// that falls out of the range of 2xx<br>
console.log(error.response.data);<br>
console.log(error.response.status);<br>
console.log(error.response.headers);<br>
} else if (error.request) {<br>
// The request was made but no response was received<br>
// `error.request` is an instance of XMLHttpRequest in the browser and an instance of<br>
// http.ClientRequest in node.js<br>
console.log(error.request);<br>
} else {<br>
// Something happened in setting up the request that triggered an Error<br>
console.log(‘Error’, error.message);<br>
}<br>
console.log(error.config);<br>
});</p>
<p>You can define a custom HTTP status code error range using the  <code>validateStatus</code>  config option.</p>
<p>axios.get(’/user/12345’, {<br>
validateStatus: function (status) {<br>
return status &lt; 500; // Reject only if the status code is greater than or equal to 500<br>
}<br>
})</p>
<h2 id="cancellation"><a href="https://github.com/axios/axios#cancellation"></a>Cancellation</h2>
<p>You can cancel a request using a  <em>cancel token</em>.</p>
<blockquote>
<p>The axios cancel token API is based on the withdrawn  <a href="https://github.com/tc39/proposal-cancelable-promises">cancelable promises proposal</a>.</p>
</blockquote>
<p>You can create a cancel token using the  <code>CancelToken.source</code>  factory as shown below:</p>
<p>var CancelToken = axios.CancelToken;<br>
var source = CancelToken.source();</p>
<p>axios.get(’/user/12345’, {<br>
cancelToken: source.token<br>
}).catch(function(thrown) {<br>
if (axios.isCancel(thrown)) {<br>
console.log(‘Request canceled’, thrown.message);<br>
} else {<br>
// handle error<br>
}<br>
});</p>
<p>axios.post(’/user/12345’, {<br>
name: ‘new name’<br>
}, {<br>
cancelToken: source.token<br>
})</p>
<p>// cancel the request (the message parameter is optional)<br>
source.cancel(‘Operation canceled by the user.’);</p>
<p>You can also create a cancel token by passing an executor function to the  <code>CancelToken</code>  constructor:</p>
<p>var CancelToken = axios.CancelToken;<br>
var cancel;</p>
<p>axios.get(’/user/12345’, {<br>
cancelToken: new CancelToken(function executor© {<br>
// An executor function receives a cancel function as a parameter<br>
cancel = c;<br>
})<br>
});</p>
<p>// cancel the request<br>
cancel();</p>
<blockquote>
<p>Note: you can cancel several requests with the same cancel token.</p>
</blockquote>
<h2 id="using-applicationx-www-form-urlencoded-format"><a href="https://github.com/axios/axios#using-applicationx-www-form-urlencoded-format"></a>Using application/x-www-form-urlencoded format</h2>
<p>By default, axios serializes JavaScript objects to  <code>JSON</code>. To send data in the  <code>application/x-www-form-urlencoded</code>  format instead, you can use one of the following options.</p>
<h3 id="browser"><a href="https://github.com/axios/axios#browser"></a>Browser</h3>
<p>In a browser, you can use the  <a href="https://developer.mozilla.org/en-US/docs/Web/API/URLSearchParams"><code>URLSearchParams</code></a>  API as follows:</p>
<p>var params = new URLSearchParams();<br>
params.append(‘param1’, ‘value1’);<br>
params.append(‘param2’, ‘value2’);<br>
axios.post(’/foo’, params);</p>
<blockquote>
<p>Note that  <code>URLSearchParams</code>  is not supported by all browsers (see  <a href="http://www.caniuse.com/#feat=urlsearchparams">caniuse.com</a>), but there is a  <a href="https://github.com/WebReflection/url-search-params">polyfill</a>  available (make sure to polyfill the global environment).</p>
</blockquote>
<p>Alternatively, you can encode data using the  <a href="https://github.com/ljharb/qs"><code>qs</code></a>  library:</p>
<p>var qs = require(‘qs’);<br>
axios.post(’/foo’, qs.stringify({ ‘bar’: 123 }));</p>
<h3 id="node.js"><a href="https://github.com/axios/axios#nodejs"></a>Node.js</h3>
<p>In node.js, you can use the  <a href="https://nodejs.org/api/querystring.html"><code>querystring</code></a>  module as follows:</p>
<p>var querystring = require(‘querystring’);<br>
axios.post(‘<a href="http://something.com/">http://something.com/</a>’, querystring.stringify({ foo: ‘bar’ }));</p>
<p>You can also use the  <a href="https://github.com/ljharb/qs"><code>qs</code></a>  library.</p>
<h2 id="semver"><a href="https://github.com/axios/axios#semver"></a>Semver</h2>
<p>Until axios reaches a  <code>1.0</code>  release, breaking changes will be released with a new minor version. For example  <code>0.5.1</code>, and  <code>0.5.4</code>  will have the same API, but  <code>0.6.0</code>  will have breaking changes.</p>
<h2 id="promises"><a href="https://github.com/axios/axios#promises"></a>Promises</h2>
<p>axios depends on a native ES6 Promise implementation to be  <a href="http://caniuse.com/promises">supported</a>. If your environment doesn’t support ES6 Promises, you can  <a href="https://github.com/jakearchibald/es6-promise">polyfill</a>.</p>
<h2 id="typescript"><a href="https://github.com/axios/axios#typescript"></a>TypeScript</h2>
<p>axios includes  <a href="http://typescriptlang.org/">TypeScript</a>  definitions.</p>
<p>import axios from ‘axios’;<br>
axios.get(’/user?ID=12345’);</p>


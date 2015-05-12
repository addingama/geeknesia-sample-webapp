# geeknesia-sample-code
This is sample code how to use geeknesia api to retrieve data using webapp with angular.js.

If you use jQuery instead of angular.js, you need to manual binding the api response with the view.

#### Sample using jQuery
Check your api key using hello api
```
$.ajax({
  method: "GET",
  url: "http://api.geeknesia.com/api/hello",
  headers: {api_key:"d5eb7e61ca97bc30692d7aec3bb5861f"}
}).done(function( msg ) {
    alert( "Response : " + msg );
});
```
Send data to server
```
$.ajax({
  method: "GET",
  url: 'http://api.geeknesia.com/api/data?api_key=d5eb7e61ca97bc30692d7aec3bb5861f&attributes={"temperature":"25"}',
}).done(function( msg ) {
    console.log(msg)
});
```
Retrieve data from server
```
$.ajax({
  method: "POST",
  url: 'http://api.geeknesia.com/api/attributes',
  headers: {
  	api_key : "d5eb7e61ca97bc30692d7aec3bb5861f"
  },
  data : {
  	limit : 10,
  	filter : "datetime", // optional
  	from : "2015-04-20T05:16:00.000Z", // date using ISO format optional
  	to :  "2015-04-21T05:16:00.000Z"// date using ISO format optional
  }
}).done(function( msg ) {
    console.log(msg)
});
```

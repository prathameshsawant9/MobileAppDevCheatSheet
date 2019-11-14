# AndroidCheatSheet
Short notes of Android SDK. Keywords to remember. 


#### ConstrainLayout 
Guidelines, Barriers, Chains and Groups
groups: contain references to view ids and can be used to hide or show views 
Guidelines: are fixed 
Barriers: are flexible and can be attached to view 
Chains Types: 
spread(---1---1---1---)
spread-inside(1-----1-----1) 
packed(-----111-----) 
// similar to linearlayout 
weighted( 1[   1   ]1 )

### Retrofit v2 
http methods : 
@Path 		  - dynamic urls or @GET Call<String> query(@Url String fileUrl);  
@Headers 	  - add headers
GET			    - Query; QueryMap
POST		    - Field; FieldMap  
Multipart 	- @Part array: Array<MultipartBody.Part> 
			        RequestBody.create(MediaType, imageFile); 
			        MultipartBody.Builder.( addFormDataPart(key, RequestBody.create) x MultipleTimes )	
  
Download Files 
@Streaming for large files 
@GET Call<ResponseBody> download(@Url String fileUrl);
responseBody.body() -> is a IOStream -> save file you normally do
  
SSL Pinning 
certificate pinner -> add(domain, "sha256/abcdefghijk") 

ssl concept : sslSocketFactory, trustmanager, CipherSuite.TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256
interceptor : http interceptor 
converters  : gson.converter, scalar converter

1. 전체 게시글 목록 조회 // sort date
<pre>
Method : GET
URL : /api/post
Request :
Response : 
{
"title": "title",
"id": "id",
"createdAt": null
}
</pre>

2. 게시글 작성
<pre>
Method : POST
URL : /api/post
Request :
{
"title": "title",
"id": "id",
"password": "password",
"content": "content",
}
Response :
{
"title": "title",
"id": :"id",
"password": "password",
"createdAt": null,
"modifiedAt": null,
"content": "content"
}
</pre>

3. 게시글 조회
<pre>
Method : GET
URL : /api/post/{id}
Request :
Response : 
{
"title": "title",
"id": "id",
"createdAt": null,
"content": "content"
}
</pre>


4. 게시글 비밀먼호 확인
<pre>
Method : POST
URL : /api/post/{id}
Request :
{
"password": "password"
}
Response : 
{
"success" : true,
"data" : true
}
</pre>

5. 게시글 수정 // 비밀번호 확인 후 맞으면 수정
<pre>
Method : PUT
URL : /api/post/{id}
Request :
{
"title": "title",
"id": "id",
"password": "password",
"content": "content",
}
Response :
{
"title": "title",
"id": :"id",
"password": "password",
"createdAt": null,
"modifiedAt": null,
"content": "content"
}
</pre>

6. 게시글 삭제 // 비밀번호 확인 후 맞으면 삭제
<pre>
Method : DELETE
URL : /api/post/{id}
Request :
{
"password": "password"
}
Response : 
{
"success" : true,
"data" : true
}
</pre>
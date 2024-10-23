+++
date = '2024-10-21T23:16:47+03:00'
draft = true
title = 'One reason to NOT server Entity'

tags = ['quality-code', 'thinks-to-avoid']
categories = ['code-philoshopher']

[params]
    author = 'George Karampelas'
+++

### Introduction 

What is the DTO, is Data Transfer Object, you use it hide fields from entity in simple words.

### Why to use it?

It is highly recomended to use DTO, for numerous reasons:

- To hide fields that are not used.
- To hide sensitive data from client.
- To be flexible on changes on future.

And more reasons that you should use DTOs, I want to stay on the last one. Most times when we implement on API and we see that the client wants exactly the entity as response we may use the entity as response on the client, with the excuse why to use mappers, create new class, etc. Let's disguss about that with an example, below is a class on Java.
```
public class Post {
    private Integer id;
    private String title;
    private String subtitle;
    private String author;
    private String content;

    // getters and setters ...
}
```
On our example you are create a news paper for a client, these is the entity on the database and is the same the response for each post, you fetch the a post, you serve a post, it works! 
But this is not mean that it is good. Your client asks for a change request that should be add some metadata on each post for other reasons. With this change the fetch of each post will be affected and you gonna create a problem that you are not gonna even see it until you test the application. But if you use a DTO you create a solid service and independet implementation from others because on entity is not used for one usage. 

### Conclusion
So using a DTO with fields that only a fetch for post, you dont have to worry that changes on your entity will break everythink.


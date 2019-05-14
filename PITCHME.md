@title[Robust, Semantic Solutions to Modern Design Challenges]

## Robust, Semantic Solutions to Modern Design Challenges

Corbb O'Connor<br>
Christina Adams

@snap[south span-50]
[http://bit.ly/robust19](http://bit.ly/robust19)
@snapend

+++
## The Conundrum
@ul
- Modern design relies upon *cutting edge* technology
- Good accessibility relies upon *well-adopted* technology
- “Bad” designer vs. the “good” developer
@ulend
+++
## The Blog Post
![Screenshot of two blog posts](images/blog-post.png)

+++
@title[The Blog Post - Order]
@snap[east span-75]
![Screenshot of two blog posts](images/blog-post.png)
@snapend

@snap[north-west span-15 text-08]
##### Likely
@ol[](false)
- Image
- Category
- Date
- Headline
- Description
- ==>
@olend
@snapend

@snap[south-west span-15 text-08]
##### Better
@ol
- Headline
- Image
- Category
- Date
- Description
- ==>
@olend
@snapend

+++
@title[The Blog Post - Code]

```html
<a class="site-card" href="/">
  <div class="blog_header">
    <h2>Top 5 Winter Adventures…</h2>
    <img src alt="A medium sized dog in a harness and leash…">
    <span>Winter Adventures</span>
    <span>1/30/2019</span>
  </div>
  <p>It is easy to give into hibernation every winter but…</p>
  <span>
    <svg version="1.1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" role="image">
      <title>Read more</title>
      <desc>Top 5 Winter Adventures…</desc>
      </svg>
  </span>
</a>
```

@[1,15](One, big link.)
@[2-8](Order we want elements to be encountered.)
@[9-15](Add the SVG.)
@[1-15]

+++
@title[The Blog Post - CSS]
```css
.blog {
  display: flex;
  flex-direction: row;
}
.blog .blog_header {
  display: flex;
  flex-direction: column;
}
.blog .blog_headline{
  order: 1;
}
.blog .blog_image {
  order: -1;
}
```
@[1-4](This containing `<div>` has `display: flex`.)
@[5-8](`Flex-direction` set to `column` so elements will stack at any viewport.)
@[9-14](Here is the real magic on how we achieved the `order`.)
@[1-14]
+++
## The Blog Post
![Screenshot of two blog posts](images/blog-post.png)

+++
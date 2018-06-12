---
layout: "post"
title: "Model Relationship Fields"
date: "2017-07-19 11:25"
categories: Django
---

### 1-N 관계
{% highlight python %}
class Post(models.Model):
  title = models.CharField(max_length=10)
  content = models.TextField()

class Comment(models.Model):
  post = models.ForeignKey(Post)
  message = models.TextField()
{% endhighlight %}

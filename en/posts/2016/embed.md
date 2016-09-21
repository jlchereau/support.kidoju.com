---
category: Developer
description: Learn how to link and embed Kidoju quizzes in any web site like a YouTube video,
icon: document_cup
keywords: Memba, Kidoju, Quizlet, Socrative, Khan Academy, education, tablets, teach, learn, knowledge, quiz, test, link, embed
language: en
title: Embed a Kidoju in your web site or blog
uuid: 3895366f-666f-4fe1-8208-96c4796a8171
author: jlchereau
author_url: https://github.com/jlchereau
avatar_url: https://avatars.githubusercontent.com/u/2556751?v=3
creation_date: 2016-04-05T05:26:53Z
edit_url: https://github.com/kidoju/support.kidoju.com/blob/master/en/posts/2016/embed.md
site_url: https://www.kidoju.com/support/en/posts/2016/04/embed
---
> Like YouTube videos and SlideShare presentations, Kidoju quizzes can be linked and embedded in any web site as shown here below.

### Example

<iframe src="https://www.kidoju.com/en/x/570cc7f46d1dd91900729417/5751b84d9bd40219006d83b1?embed=true&theme=default" style="height:500px;width:100%;border:solid 1px #d5d5d5;"></iframe>

### How to, step by step

To embed a quiz in your web site, first display the quiz details and click the **Embed** tab of the  **Share** panel:

![Summary Page](https://raw.githubusercontent.com/kidoju/support.kidoju.com/master/en/posts/2016/embed.png)

Then simply copy and paste the code within your html page as in: 

```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Title</title>
</head>
<body>
<iframe src="https://www.kidoju.com/en/x/570cc7f46d1dd91900729417/5751b84d9bd40219006d83b1?embed=true&theme=default"
style="height:494px;width:100%;border:solid 1px #d5d5d5"></iframe>
</body>
</html>
```


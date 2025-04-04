---
title: Comment.dateTimeUtc property
linktitle: dateTimeUtc property
articleTitle: dateTimeUtc property
second_title: Aspose.Words for Node.js
description: "Comment.dateTimeUtc property. Gets the UTC date and time that the comment was made."
type: docs
weight: 50
url: /nodejs-net/aspose.words/comment/dateTimeUtc/
---

## Comment.dateTimeUtc property

Gets the UTC date and time that the comment was made.


```js
get dateTimeUtc(): Date
```

### Remarks

The default value is
datetime.datetime.min



### Examples

Shows how to get UTC date and time.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let date = new Date(2021, 9, 21, 10, 0, 0);

let comment = new aw.Comment(doc, "John Doe", "J.D.", date);
comment.setText("My comment.");


builder.currentParagraph.appendChild(comment);

doc.save(base.artifactsDir + "Comment.UtcDateTime.docx");
doc = new aw.Document(base.artifactsDir + "Comment.UtcDateTime.docx");

comment = doc.getComment(0, true);
// DateTimeUtc return data without milliseconds.
let expected = moment(date).add(date.getTimezoneOffset(), 'm').toDate();
expect(comment.dateTimeUtc).toEqual(expected);
```

### See Also

* module [Aspose.Words](../../)
* class [Comment](../)


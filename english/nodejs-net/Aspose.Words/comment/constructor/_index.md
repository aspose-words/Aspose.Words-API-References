---
title: Comment constructor
linktitle: Comment constructor
articleTitle: Comment constructor
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Comment constructor"
type: docs
weight: 10
url: /nodejs-net/Aspose.Words/comment/constructor/
---

## Comment(doc) {#documentbase}

Initializes a new instance of the [Comment](../) class.



```js
Comment(doc: Aspose.Words.DocumentBase)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../documentbase/) | The owner document. |

### Remarks

When [Comment](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parentNode](../../node/parentNode/) is ``None``.

To append [Comment](../) to the document use [CompositeNode.insertAfter()](../../compositenode/insertAfter/#node_node) or [CompositeNode.insertBefore()](../../compositenode/insertBefore/#node_node)
on the paragraph where you want the comment inserted.

After creating a comment, don't forget to set its [Comment.author](../author/),
[Comment.initial](../initial/) and [Comment.dateTime](../dateTime/) properties.




## Comment(doc, author, initial, dateTime) {#documentbase_string_string_date}

Initializes a new instance of the [Comment](../) class.



```js
Comment(doc: Aspose.Words.DocumentBaseauthor: stringinitial: stringdateTime: Date)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../documentbase/) | The owner document. |
| author | string | The author name for the comment. Cannot be ``None``. |
| initial | string | The author initials for the comment. Cannot be ``None``. |
| dateTime | Date | The date and time for the comment. |

## See Also

* module [Aspose.Words](../../)
* class [Comment](../)


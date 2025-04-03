---
title: Run constructor
linktitle: Run constructor
articleTitle: Run constructor
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Run constructor"
type: docs
weight: 10
url: /nodejs-net/Aspose.Words/run/constructor/
---

## Run(doc) {#documentbase}

Initializes a new instance of the [Run](../) class.



```js
Run(doc: Aspose.Words.DocumentBase)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../documentbase/) | The owner document. |

### Remarks

When [Run](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parentNode](../../node/parentNode/) is ``null``.

To append [Run](../) to the document use [CompositeNode.insertAfter()](../../compositenode/insertAfter/#node_node) or [CompositeNode.insertBefore()](../../compositenode/insertBefore/#node_node)
on the paragraph where you want the run inserted.




## Run(doc, text) {#documentbase_string}

Initializes a new instance of the **Run** class.



```js
Run(doc: Aspose.Words.DocumentBasetext: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../documentbase/) | The owner document. |
| text | string | The text of the run. |

### Remarks

When [Run](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parentNode](../../node/parentNode/) is ``null``.

To append [Run](../) to the document use [CompositeNode.insertAfter()](../../compositenode/insertAfter/#node_node) or [CompositeNode.insertBefore()](../../compositenode/insertBefore/#node_node)
on the paragraph where you want the run inserted.




## See Also

* module [Aspose.Words](../../)
* class [Run](../)


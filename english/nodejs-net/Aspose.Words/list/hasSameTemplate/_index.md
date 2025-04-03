---
title: List.hasSameTemplate method
linktitle: hasSameTemplate method
articleTitle: hasSameTemplate method
second_title: Aspose.Words for NodeJs
description: "List.hasSameTemplate method. Returns true if the current list and the given list are created from the same template."
type: docs
weight: 110
url: /nodejs-net/aspose.words/list/hasSameTemplate/
---

## hasSameTemplate(other) {#list}

Returns true if the current list and the given list are created from the same template.


```js
hasSameTemplate(other: Aspose.Words.Lists.List)
```

| Parameter | Type | Description |
| --- | --- | --- |
| other | [List](../) |  |

### Examples

Shows how to define lists with the same ListDefId.

```js
let doc = new aw.Document(base.myDir + "Different lists.docx");

expect(doc.lists.at(0).hasSameTemplate(doc.lists.at(1))).toEqual(true);
expect(doc.lists.at(1).hasSameTemplate(doc.lists.at(2))).toEqual(false);
```

### See Also

* module [Aspose.Words](../../)
* class [List](../)


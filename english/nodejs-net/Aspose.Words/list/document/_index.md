---
title: List.document property
linktitle: document property
articleTitle: document property
second_title: Aspose.Words for NodeJs
description: "List.document property. Gets the owner document."
type: docs
weight: 10
url: /nodejs-net/aspose.words/list/document/
---

## List.document property

Gets the owner document.


```js
get document(): Aspose.Words.DocumentBase
```

### Remarks

A list always has a parent document and is valid only in the context of that document.




### Examples

Shows how to verify owner document properties of lists.

```js
let doc = new aw.Document();

let lists = doc.lists;
expect(lists.document.referenceEquals(doc)).toEqual(true);

let list = lists.add(aw.Lists.ListTemplate.BulletDefault);
expect(list.document.referenceEquals(doc)).toBe(true);

console.log("Current list count: " + lists.count);
console.log("Is the first document list: " + (lists.at(0).equals(list)));
console.log("ListId: " + list.listId);
console.log("List is the same by ListId: " + (lists.getListByListId(1).equals(list)));
```

### See Also

* module [Aspose.Words](../../)
* class [List](../)


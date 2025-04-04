---
title: ListCollection.document property
linktitle: document property
articleTitle: document property
second_title: Aspose.Words for Node.js
description: "ListCollection.document property. Gets the owner document."
type: docs
weight: 20
url: /nodejs-net/aspose.words.lists/listcollection/document/
---

## ListCollection.document property

Gets the owner document.


```js
get document(): Aspose.Words.DocumentBase
```

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

* module [Aspose.Words.Lists](../../)
* class [ListCollection](../)


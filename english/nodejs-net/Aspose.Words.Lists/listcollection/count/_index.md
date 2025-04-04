---
title: ListCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Node.js
description: "ListCollection.count property. Gets the count of numbered and bulleted lists in the document."
type: docs
weight: 10
url: /nodejs-net/aspose.words.lists/listcollection/count/
---

## ListCollection.count property

Gets the count of numbered and bulleted lists in the document.


```js
get count(): number
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


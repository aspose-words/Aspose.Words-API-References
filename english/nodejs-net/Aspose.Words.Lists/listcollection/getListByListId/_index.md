---
title: ListCollection.getListByListId method
linktitle: getListByListId method
articleTitle: getListByListId method
second_title: Aspose.Words for Node.js
description: "ListCollection.getListByListId method. Gets a list by a list identifier."
type: docs
weight: 70
url: /nodejs-net/aspose.words.lists/listcollection/getListByListId/
---

## getListByListId(listId) {#number}

Gets a list by a list identifier.


```js
getListByListId(listId: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| listId | number | The list identifier. |

### Remarks

You don't normally need to use this method. Most of the time you apply list formatting
to paragraphs just by settings the [ListFormat.list](../../listformat/list/) property
of the [ListFormat](../../listformat/) object.




### Returns

Returns the list object. Returns ``null`` if a list with the specified identifier was not found.


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


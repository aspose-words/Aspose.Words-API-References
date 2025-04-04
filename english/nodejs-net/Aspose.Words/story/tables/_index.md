---
title: Story.tables property
linktitle: tables property
articleTitle: tables property
second_title: Aspose.Words for Node.js
description: "Story.tables property. Gets a collection of tables that are immediate children of the story."
type: docs
weight: 50
url: /nodejs-net/aspose.words/story/tables/
---

## Story.tables property

Gets a collection of tables that are immediate children of the story.


```js
get tables(): Aspose.Words.Tables.TableCollection
```

### Examples

Shows how to remove the first and last rows of all tables in a document.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");

let tables = doc.firstSection.body.tables.toArray();

expect(tables[0].rows.count).toEqual(5);
expect(tables[1].rows.count).toEqual(4);

for (var table of tables)
{
  table.firstRow?.remove();
  table.lastRow?.remove();
}

expect(tables[0].rows.count).toEqual(3);
expect(tables[1].rows.count).toEqual(2);
```

### See Also

* module [Aspose.Words](../../)
* class [Story](../)


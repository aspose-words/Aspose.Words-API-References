---
title: FieldStart.fieldData property
linktitle: fieldData property
articleTitle: fieldData property
second_title: Aspose.Words for NodeJs
description: "FieldStart.fieldData property. Gets custom field data which is associated with the field."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Fields/fieldstart/fieldData/
---

## FieldStart.fieldData property

Gets custom field data which is associated with the field.


```js
get fieldData(): number[]
```

### Examples

Shows how to get data associated with the field.

```js
let doc = new aw.Document(base.myDir + "Field sample - Field with data.docx");

let field = doc.range.fields.at(2);
console.log(new Buffer.from(field.start.fieldData).toString('utf-8'));
```

### See Also

* module [Aspose.Words.Fields](../../)
* class [FieldStart](../)


---
title: Field.displayResult property
linktitle: displayResult property
articleTitle: displayResult property
second_title: Aspose.Words for Node.js
description: "Field.displayResult property. Gets the text that represents the displayed field result."
type: docs
weight: 10
url: /nodejs-net/aspose.words/field/displayResult/
---

## Field.displayResult property

Gets the text that represents the displayed field result.


```js
get displayResult(): string
```

### Remarks

The [Document.updateListLabels()](../../document/updateListLabels/#default) method must be called to obtain correct value for the
[FieldListNum](../../../aspose.words.fields/fieldlistnum/), [FieldAutoNum](../../../aspose.words.fields/fieldautonum/), [FieldAutoNumOut](../../../aspose.words.fields/fieldautonumout/) and [FieldAutoNumLgl](../../../aspose.words.fields/fieldautonumlgl/) fields.



### Examples

Shows how to get the real text that a field displays in the document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("This document was written by ");
let fieldAuthor = builder.insertField(aw.Fields.FieldType.FieldAuthor, true).asFieldAuthor();
fieldAuthor.authorName = "John Doe";

// We can use the DisplayResult property to verify what exact text
// a field would display in its place in the document.
expect(fieldAuthor.displayResult).toEqual('');

// Fields do not maintain accurate result values in real-time. 
// To make sure our fields display accurate results at any given time,
// such as right before a save operation, we need to update them manually.
fieldAuthor.update();

expect(fieldAuthor.displayResult).toEqual("John Doe");

doc.save(base.artifactsDir + "Field.displayResult.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Field](../)


---
title: FieldBuilder.buildAndInsert method
linktitle: buildAndInsert method
articleTitle: buildAndInsert method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Fields.FieldBuilder.buildAndInsert method"
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Fields/fieldbuilder/buildAndInsert/
---

## buildAndInsert(refNode) {#inline}

Builds and inserts a field into the document before the specified inline node.


```js
buildAndInsert(refNode: Aspose.Words.Inline)
```

| Parameter | Type | Description |
| --- | --- | --- |
| refNode | [Inline](../../../Aspose.Words/inline/) |  |

### Returns

A [Field](../../../Aspose.Words/field/) object that represents the inserted field.


## buildAndInsert(refNode) {#paragraph}

Builds and inserts a field into the document to the end of the specified paragraph.


```js
buildAndInsert(refNode: Aspose.Words.Paragraph)
```

| Parameter | Type | Description |
| --- | --- | --- |
| refNode | [Paragraph](../../../Aspose.Words/paragraph/) |  |

### Returns

A [Field](../../../Aspose.Words/field/) object that represents the inserted field.


## Examples

Shows how to create and insert a field using a field builder.

```js
let doc = new aw.Document();

// A convenient way of adding text content to a document is with a document builder.
let builder = new aw.DocumentBuilder(doc);
builder.write(" Hello world! This text is one Run, which is an inline node.");

// Fields have their builder, which we can use to construct a field code piece by piece.
// In this case, we will construct a BARCODE field representing a US postal code,
// and then insert it in front of a Run.
let fieldBuilder = new aw.Fields.FieldBuilder(aw.Fields.FieldType.FieldBarcode);
fieldBuilder.addArgument("90210");
fieldBuilder.addSwitch("\\f", "A");
fieldBuilder.addSwitch("\\u");

fieldBuilder.buildAndInsert(doc.firstSection.body.firstParagraph.runs.at(0));

doc.updateFields();
doc.save(base.artifactsDir + "Field.CreateWithFieldBuilder.docx");
```

## See Also

* module [Aspose.Words.Fields](../../)
* class [FieldBuilder](../)


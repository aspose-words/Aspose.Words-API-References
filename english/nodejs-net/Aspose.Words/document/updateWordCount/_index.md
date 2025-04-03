---
title: Document.updateWordCount method
linktitle: updateWordCount method
articleTitle: updateWordCount method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Document.updateWordCount method"
type: docs
weight: 800
url: /nodejs-net/Aspose.Words/document/updateWordCount/
---

## updateWordCount() {#default}

Updates word count properties of the document.


```js
updateWordCount()
```

### Remarks

[Document.updateWordCount()](./#default) recalculates and updates Characters, Words and Paragraphs
properties in the [Document.builtInDocumentProperties](../builtInDocumentProperties/) collection of the [Document](../).

Note that [Document.updateWordCount()](./#default) does not update number of lines and pages properties.
Use the [Document.updateWordCount()](./#default) overload and pass ``true`` value as a parameter to do that.

When you use an evaluation version, the evaluation watermark will also be included
in the word count.




## updateWordCount(updateLinesCount) {#boolean}

Updates word count properties of the document, optionally updates [BuiltInDocumentProperties.lines](../../../aspose.words.properties/builtindocumentproperties/lines/) property.



```js
updateWordCount(updateLinesCount: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| updateLinesCount | boolean | ``true`` if number of lines in the document shall be calculated. |

### Remarks

This method will rebuild page layout of the document.


## Examples

Shows how to update all list labels in a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");
// Aspose.words does not track document metrics like these in real time.
expect(doc.builtInDocumentProperties.characters).toEqual(0);
expect(doc.builtInDocumentProperties.words).toEqual(0);
expect(doc.builtInDocumentProperties.paragraphs).toEqual(1);
expect(doc.builtInDocumentProperties.lines).toEqual(1);
// To get accurate values for three of these properties, we will need to update them manually.
doc.updateWordCount();
expect(doc.builtInDocumentProperties.characters).toEqual(196);
expect(doc.builtInDocumentProperties.words).toEqual(36);
expect(doc.builtInDocumentProperties.paragraphs).toEqual(2);
// For the line count, we will need to call a specific overload of the updating method.
expect(doc.builtInDocumentProperties.lines).toEqual(1);
doc.updateWordCount(true);
expect(doc.builtInDocumentProperties.lines).toEqual(4);
```

## See Also

* module [Aspose.Words](../../)
* class [Document](../)


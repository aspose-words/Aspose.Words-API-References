---
title: TxtSaveOptions.simplifyListLabels property
linktitle: simplifyListLabels property
articleTitle: simplifyListLabels property
second_title: Aspose.Words for NodeJs
description: "TxtSaveOptions.simplifyListLabels property. Specifies whether the program should simplify list labels in case of complex label formatting not being adequately represented by plain text."
type: docs
weight: 70
url: /nodejs-net/Aspose.Words.Saving/txtsaveoptions/simplifyListLabels/
---

## TxtSaveOptions.simplifyListLabels property

Specifies whether the program should simplify list labels in case of
complex label formatting not being adequately represented by plain text.

If set to ``True``, numbered list labels are written in simple numeric format
and itemized list labels as simple ASCII characters. The default value is ``False``.




```js
get simplifyListLabels(): boolean
```

### Examples

Shows how to change the appearance of lists when saving a document to plaintext.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Create a bulleted list with five levels of indentation.
builder.listFormat.applyBulletDefault();
builder.writeln("Item 1");
builder.listFormat.listIndent();
builder.writeln("Item 2");
builder.listFormat.listIndent();
builder.writeln("Item 3");
builder.listFormat.listIndent();
builder.writeln("Item 4");
builder.listFormat.listIndent();
builder.write("Item 5");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
let txtSaveOptions = new aw.Saving.TxtSaveOptions();

// Set the "SimplifyListLabels" property to "true" to convert some list
// symbols into simpler ASCII characters, such as '*', 'o', '+', '>', etc.
// Set the "SimplifyListLabels" property to "false" to preserve as many original list symbols as possible.
txtSaveOptions.simplifyListLabels = simplifyListLabels;

doc.save(base.artifactsDir + "TxtSaveOptions.simplifyListLabels.txt", txtSaveOptions);

let docText = readTextFile(base.artifactsDir + "TxtSaveOptions.simplifyListLabels.txt");

if (simplifyListLabels)
  expect(docText).toEqual("* Item 1\r\n" +
                            "  > Item 2\r\n" +
                            "    + Item 3\r\n" +
                            "      - Item 4\r\n" +
                            "        o Item 5\r\n");
else
  expect(docText).toEqual("· Item 1\r\n" +
                            "o Item 2\r\n" +
                            "§ Item 3\r\n" +
                            "· Item 4\r\n" +
                            "o Item 5\r\n");
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [TxtSaveOptions](../)


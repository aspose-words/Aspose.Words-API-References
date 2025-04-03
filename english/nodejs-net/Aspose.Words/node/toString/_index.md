---
title: Node.toString method
linktitle: toString method
articleTitle: toString method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Node.toString method"
type: docs
weight: 510
url: /nodejs-net/Aspose.Words/node/toString/
---

## toString(saveFormat) {#saveformat}

Exports the content of the node into a string in the specified format.


```js
toString(saveFormat: Aspose.Words.SaveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | [SaveFormat](../../saveformat/) |  |

### Returns

The content of the node in the specified format.


## toString(saveOptions) {#saveoptions}

Exports the content of the node into a string using the specified save options.


```js
toString(saveOptions: Aspose.Words.Saving.SaveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../../aspose.words.saving/saveoptions/) | Specifies the options that control how the node is saved. |

### Returns

The content of the node in the specified format.


## Examples

Shows the difference between calling the GetText and ToString methods on a node.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.insertField("MERGEFIELD Field");
// GetText will retrieve the visible text as well as field codes and special characters.
expect(doc.getText().trim()).toEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015");
// ToString will give us the document's appearance if saved to a passed save format.
expect(doc.toString(aw.SaveFormat.Text).trim()).toEqual("«Field»");
```

Exports the content of a node to String in HTML format.

```js
let doc = new aw.Document(base.myDir + "Document.docx");

let node = doc.lastSection.body.lastParagraph;

// When we call the ToString method using the html SaveFormat overload,
// it converts the node's contents to their raw html representation.
expect(node.toString(aw.SaveFormat.Html)).toEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                        "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                        "</p>");

// We can also modify the result of this conversion using a SaveOptions object.
let saveOptions = new aw.Saving.HtmlSaveOptions();
saveOptions.exportRelativeFontSize = true;

expect(node.toString(saveOptions)).toEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                        "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                        "</p>");
```

Shows how to extract the list labels of all paragraphs that are list items.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");
doc.updateListLabels();

let paras = doc.getChildNodes(aw.NodeType.Paragraph, true).toArray();

// Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
// which start at three and ends at six.
for (let node of paras.filter(p => p.asParagraph().listFormat.isListItem))
{
  let paragraph = node.asParagraph();
  console.log(`List item paragraph #${paras.indexOf(paragraph)}`);

  // This is the text we get when getting when we output this node to text format.
  // This text output will omit list labels. Trim any paragraph formatting characters. 
  let paragraphText = paragraph.toString(aw.SaveFormat.Text).trim();
  console.log(`\tExported Text: ${paragraphText}`);

  let label = paragraph.listLabel;

  // This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
  // this will tell us what position it is on that level.
  console.log(`\tNumerical Id: ${label.labelValue}`);

  // Combine them together to include the list label with the text in the output.
  console.log(`\tList label combined with text: ${label.labelString} ${paragraphText}`);
}
```

## See Also

* module [Aspose.Words](../../)
* class [Node](../)


---
title: Document.updateListLabels method
linktitle: updateListLabels method
articleTitle: updateListLabels method
second_title: Aspose.Words for Node.js
description: "Document.updateListLabels method. Updates list labels for all list items in the document."
type: docs
weight: 770
url: /nodejs-net/aspose.words/document/updateListLabels/
---

## updateListLabels() {#default}

Updates list labels for all list items in the document.


```js
updateListLabels()
```

### Remarks

This method updates list label properties such as [ListLabel.labelValue](../../../aspose.words.lists/listlabel/labelValue/) and
[ListLabel.labelString](../../../aspose.words.lists/listlabel/labelString/) for each [Paragraph.listLabel](../../paragraph/listLabel/) object in the document.

Also, this method is sometimes implicitly called when updating fields in the document. This is required
because some fields that may reference list numbers (such as TOC or REF) need them be up-to-date.




### Examples

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

### See Also

* module [Aspose.Words](../../)
* class [Document](../)


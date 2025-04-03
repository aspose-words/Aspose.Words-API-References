---
title: ListLabel class
linktitle: ListLabel class
articleTitle: ListLabel class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Lists.ListLabel class. Defines properties specific to a list label"
type: docs
weight: 30
url: /nodejs-net/aspose.words.lists/listlabel/
---

## ListLabel class

Defines properties specific to a list label.
To learn more, visit the [Working with Lists](https://docs.aspose.com/words/nodejs-net/working-with-lists/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [font](./font/) | Gets the list label font. |
| [labelString](./labelString/) | Gets a string representation of list label. |
| [labelValue](./labelValue/) | Gets a numeric value for this label. |

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

* module [Aspose.Words.Lists](../)


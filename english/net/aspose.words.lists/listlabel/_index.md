---
title: ListLabel Class
linktitle: ListLabel
articleTitle: ListLabel
second_title: Aspose.Words for .NET
description: Aspose.Words.Lists.ListLabel class. Defines properties specific to a list label in C#.
type: docs
weight: 3790
url: /net/aspose.words.lists/listlabel/
---
## ListLabel class

Defines properties specific to a list label.

To learn more, visit the [Working with Lists](https://docs.aspose.com/words/net/working-with-lists/) documentation article.

```csharp
public class ListLabel
```

## Properties

| Name | Description |
| --- | --- |
| [Font](../../aspose.words.lists/listlabel/font/) { get; } | Gets the list label font. |
| [LabelString](../../aspose.words.lists/listlabel/labelstring/) { get; } | Gets a string representation of list label. |
| [LabelValue](../../aspose.words.lists/listlabel/labelvalue/) { get; } | Gets a numeric value for this label. |

## Examples

Shows how to extract the list labels of all paragraphs that are list items.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
// which start at three and ends at six.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // This is the text we get when getting when we output this node to text format.
    // This text output will omit list labels. Trim any paragraph formatting characters. 
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
    // this will tell us what position it is on that level.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Combine them together to include the list label with the text in the output.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### See Also

* namespace [Aspose.Words.Lists](../../aspose.words.lists/)
* assembly [Aspose.Words](../../)

---
title: Paragraph.ListLabel
linktitle: ListLabel
articleTitle: ListLabel
second_title: Aspose.Words for .NET
description: Access and format list numbering with the Paragraph ListLabel property. Enhance your document's organization and clarity effortlessly!
type: docs
weight: 160
url: /net/aspose.words/paragraph/listlabel/
---
## Paragraph.ListLabel property

Gets a `ListLabel` object that provides access to list numbering value and formatting for this paragraph.

```csharp
public ListLabel ListLabel { get; }
```

## Examples

Shows how to extract the list labels of all paragraphs that are list items.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
// which start at three and ends at six.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
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

* class [ListLabel](../../../aspose.words.lists/listlabel/)
* class [Paragraph](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

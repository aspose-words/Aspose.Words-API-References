---
title: Document.UpdateListLabels
linktitle: UpdateListLabels
articleTitle: UpdateListLabels
second_title: Aspose.Words for .NET
description: Effortlessly update all list item labels in your document with the UpdateListLabels method, ensuring consistency and clarity in your content.
type: docs
weight: 820
url: /net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

Updates list labels for all list items in the document.

```csharp
public void UpdateListLabels()
```

## Remarks

This method updates list label properties such as [`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) and [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/) for each [`ListLabel`](../../paragraph/listlabel/) object in the document.

Also, this method is sometimes implicitly called when updating fields in the document. This is required because some fields that may reference list numbers (such as TOC or REF) need them be up-to-date.

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

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---
title: Node.ToString
linktitle: ToString
articleTitle: ToString
second_title: Aspose.Words for .NET
description: Discover the Node ToString method, effortlessly convert node content into strings with customizable formats for enhanced data handling. Optimize your coding today!
type: docs
weight: 160
url: /net/aspose.words/node/tostring/
---
## ToString(*[SaveFormat](../../saveformat/)*) {#tostring_1}

Exports the content of the node into a string in the specified format.

```csharp
public string ToString(SaveFormat saveFormat)
```

### Return Value

The content of the node in the specified format.

## Examples

Shows the difference between calling the GetText and ToString methods on a node.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText will retrieve the visible text as well as field codes and special characters.
Assert.That(doc.GetText().Trim(), Is.EqualTo("\u0013MERGEFIELD Field\u0014«Field»\u0015"));

// ToString will give us the document's appearance if saved to a passed save format.
Assert.That(doc.ToString(SaveFormat.Text).Trim(), Is.EqualTo("«Field»"));
```

Exports the content of a node to String in HTML format.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// When we call the ToString method using the html SaveFormat overload,
// it converts the node's contents to their raw html representation.
Assert.That(node.ToString(SaveFormat.Html), Is.EqualTo("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>"));

// We can also modify the result of this conversion using a SaveOptions object.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.That(node.ToString(saveOptions), Is.EqualTo("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>"));
```

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

* enum [SaveFormat](../../saveformat/)
* class [Node](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## ToString(*[SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#tostring_2}

Exports the content of the node into a string using the specified save options.

```csharp
public string ToString(SaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| saveOptions | SaveOptions | Specifies the options that control how the node is saved. |

### Return Value

The content of the node in the specified format.

## Examples

Exports the content of a node to String in HTML format.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// When we call the ToString method using the html SaveFormat overload,
// it converts the node's contents to their raw html representation.
Assert.That(node.ToString(SaveFormat.Html), Is.EqualTo("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>"));

// We can also modify the result of this conversion using a SaveOptions object.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.That(node.ToString(saveOptions), Is.EqualTo("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>"));
```

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Node](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

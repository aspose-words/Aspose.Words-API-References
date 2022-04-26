---
title: SmartTag
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 3710
url: /net/aspose.words.markup/smarttag/
---
## SmartTag class

This element specifies the presence of a smart tag around one or more inline structures (runs, images, fields,etc.) within a paragraph.

```csharp
public class SmartTag : CompositeNode
```

## Constructors

| Name | Description |
| --- | --- |
| [SmartTag](smarttag)(DocumentBase) | Initializes a new instance of the [`SmartTag`](../smarttag) class. |

## Properties

| Name | Description |
| --- | --- |
| [Element](element) { get; set; } | Specifies the name of the smart tag within the document. |
| override [NodeType](nodetype) { get; } | Returns **NodeType.SmartTag**. |
| [Properties](properties) { get; } | A collection of the smart tag properties. |
| [Uri](uri) { get; set; } | Specifies the namespace URI of the smart tag. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](accept)(DocumentVisitor) | Accepts a visitor. |

### Remarks

Smart tags is a kind of custom XML markup. Smart tags provide a facility for embedding customer-defined semantics into the document via the ability to provide a basic namespace/name for a run or set of runs within a document.

[`SmartTag`](../smarttag) can be a child of a [`Paragraph`](../../aspose.words/paragraph) or another [`SmartTag`](../smarttag) node.

The complete list of child nodes that can occur inside a smart tag consists of [`BookmarkStart`](../../aspose.words/bookmarkstart), [`BookmarkEnd`](../../aspose.words/bookmarkend), [`FieldStart`](../../aspose.words.fields/fieldstart), [`FieldSeparator`](../../aspose.words.fields/fieldseparator), [`FieldEnd`](../../aspose.words.fields/fieldend), [`FormField`](../../aspose.words.fields/formfield), [`Comment`](../../aspose.words/comment), [`Footnote`](../../aspose.words.notes/footnote), [`Run`](../../aspose.words/run), [`SpecialChar`](../../aspose.words/specialchar), [`Shape`](../../aspose.words.drawing/shape), [`GroupShape`](../../aspose.words.drawing/groupshape), [`CommentRangeStart`](../../aspose.words/commentrangestart), [`CommentRangeEnd`](../../aspose.words/commentrangeend), [`SmartTag`](../smarttag).

### Examples

Shows how to create smart tags.

```csharp
public void Create()
{
    Document doc = new Document();

    // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
    // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
    SmartTag smartTag = new SmartTag(doc);

    // Smart tags are composite nodes that contain their recognized text in its entirety.
    // Add contents to this smart tag manually.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word may recognize the above contents as being a date.
    // Smart tags use the "Element" property to reflect the type of data they contain.
    smartTag.Element = "date";

    // Some smart tag types process their contents further into custom XML properties.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // Set the smart tag's URI to the default value.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // Create another smart tag for a stock ticker.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // Print all the smart tags in our document using a document visitor.
    doc.Accept(new SmartTagPrinter());

    // Older versions of Microsoft Word support smart tags.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // Use the "RemoveSmartTags" method to remove all smart tags from a document.
    Assert.AreEqual(2, doc.GetChildNodes(NodeType.SmartTag, true).Count);

    doc.RemoveSmartTags();

    Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
}

/// <summary>
/// Prints visited smart tags and their contents.
/// </summary>
private class SmartTagPrinter : DocumentVisitor
{
    /// <summary>
    /// Called when a SmartTag node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        Console.WriteLine($"Smart tag type: {smartTag.Element}");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when the visiting of a SmartTag node is ended.
    /// </summary>
    public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
    {
        Console.WriteLine($"\tContents: \"{smartTag.ToString(SaveFormat.Text)}\"");

        if (smartTag.Properties.Count == 0)
        {
            Console.WriteLine("\tContains no properties");
        }
        else
        {
            Console.Write("\tProperties: ");
            string[] properties = new string[smartTag.Properties.Count];
            int index = 0;

            foreach (CustomXmlProperty cxp in smartTag.Properties)
                properties[index++] = $"\"{cxp.Name}\" = \"{cxp.Value}\"";

            Console.WriteLine(string.Join(", ", properties));
        }

        return VisitorAction.Continue;
    }
}
```

### See Also

* class [CompositeNode](../../aspose.words/compositenode)
* namespace [Aspose.Words.Markup](../../aspose.words.markup)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

---
title: CustomXmlProperty
linktitle: CustomXmlProperty
articleTitle: CustomXmlProperty
second_title: Aspose.Words for .NET
description: Discover the CustomXmlProperty constructor. Easily create and initialize new instances for seamless XML property management in your projects.
type: docs
weight: 10
url: /net/aspose.words.markup/customxmlproperty/customxmlproperty/
---
## CustomXmlProperty constructor

Initializes a new instance of this class.

```csharp
public CustomXmlProperty(string name, string uri, string value)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | The name of the property. Cannot be `null`. |
| uri | String | The namespace URI of the property. Cannot be `null`. |
| value | String | The value of the property. Cannot be `null`. |

## Examples

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
    Assert.That(doc.GetChildNodes(NodeType.SmartTag, true).Count, Is.EqualTo(2));

    doc.RemoveSmartTags();

    Assert.That(doc.GetChildNodes(NodeType.SmartTag, true).Count, Is.EqualTo(0));
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

* class [CustomXmlProperty](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)

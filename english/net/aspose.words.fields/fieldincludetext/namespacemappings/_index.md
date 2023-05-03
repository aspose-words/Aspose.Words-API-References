---
title: FieldIncludeText.NamespaceMappings
linktitle: NamespaceMappings
articleTitle: NamespaceMappings
second_title: Aspose.Words for .NET API Reference
description: FieldIncludeText NamespaceMappings property. Gets or sets the namespace mappings for XPath queries in C#.
type: docs
weight: 60
url: /net/aspose.words.fields/fieldincludetext/namespacemappings/
---
## FieldIncludeText.NamespaceMappings property

Gets or sets the namespace mappings for XPath queries.

```csharp
public string NamespaceMappings { get; set; }
```

## Examples

Shows how to create an INCLUDETEXT field, and set its properties.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
    // 1 -  Perform an XSL transformation on an XML document:
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2 -  Use an XPath to take specific elements from an XML document:
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");
}

/// <summary>
/// Use a document builder to insert an INCLUDETEXT field with custom properties.
/// </summary>
public FieldIncludeText CreateFieldIncludeText(DocumentBuilder builder, string sourceFullName, bool lockFields, string mimeType, string textConverter, string encoding)
{
    FieldIncludeText fieldIncludeText = (FieldIncludeText)builder.InsertField(FieldType.FieldIncludeText, true);
    fieldIncludeText.SourceFullName = sourceFullName;
    fieldIncludeText.LockFields = lockFields;
    fieldIncludeText.MimeType = mimeType;
    fieldIncludeText.TextConverter = textConverter;
    fieldIncludeText.Encoding = encoding;

    return fieldIncludeText;
}
```

### See Also

* class [FieldIncludeText](../)
* namespace [Aspose.Words.Fields](../../fieldincludetext/)
* assembly [Aspose.Words](../../../)

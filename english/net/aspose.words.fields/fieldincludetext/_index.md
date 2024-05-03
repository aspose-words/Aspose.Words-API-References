---
title: FieldIncludeText Class
linktitle: FieldIncludeText
articleTitle: FieldIncludeText
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FieldIncludeText class. Implements the INCLUDETEXT field in C#.
type: docs
weight: 2250
url: /net/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class

Implements the INCLUDETEXT field.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class FieldIncludeText : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldIncludeText](fieldincludetext/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldincludetext/bookmarkname/) { get; set; } | Gets or sets the name of the bookmark in the document to include. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Gets the text that represents the displayed field result. |
| [Encoding](../../aspose.words.fields/fieldincludetext/encoding/) { get; set; } | Gets or sets the encoding applied to the data within the referenced file. |
| [End](../../aspose.words.fields/field/end/) { get; } | Gets the node that represents the field end. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Gets a [`FieldFormat`](../fieldformat/) object that provides typed access to field's formatting. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Gets or sets the LCID of the field. |
| [LockFields](../../aspose.words.fields/fieldincludetext/lockfields/) { get; set; } | Gets or sets whether to prevent fields in the included document from being updated. |
| [MimeType](../../aspose.words.fields/fieldincludetext/mimetype/) { get; set; } | Gets or sets the MIME type of the referenced file. |
| [NamespaceMappings](../../aspose.words.fields/fieldincludetext/namespacemappings/) { get; set; } | Gets or sets the namespace mappings for XPath queries. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Gets the node that represents the field separator. Can be `null`. |
| [SourceFullName](../../aspose.words.fields/fieldincludetext/sourcefullname/) { get; set; } | Gets or sets the location of the document using an IRI. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Gets the node that represents the start of the field. |
| [TextConverter](../../aspose.words.fields/fieldincludetext/textconverter/) { get; set; } | Gets or sets the name of the text converter for the format of the included file. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Gets the Microsoft Word field type. |
| [XPath](../../aspose.words.fields/fieldincludetext/xpath/) { get; set; } | Gets or sets XPath for the desired portion of the XML file. |
| [XslTransformation](../../aspose.words.fields/fieldincludetext/xsltransformation/) { get; set; } | Gets or sets the location of XSL Transformation to format XML data. |

## Methods

| Name | Description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../../aspose.words.fields/field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns `null`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Performs the field unlink. |
| [Update](../../aspose.words.fields/field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Performs a field update. Throws if the field is being updated already. |

## Remarks

Inserts all or part of the text and graphics contained in another document.

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

* class [Field](../field/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)

---
title: BuiltInDocumentProperties
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 4140
url: /net/aspose.words.properties/builtindocumentproperties/
---
## BuiltInDocumentProperties class

A collection of built-in document properties.

```csharp
public class BuiltInDocumentProperties : DocumentPropertyCollection
```

## Public Members

| Name | Description |
| --- | --- |
| [Author](author) { get; set; } | Gets or sets the name of the document's author. |
| [Bytes](bytes) { get; set; } | Represents an estimate of the number of bytes in the document. |
| [Category](category) { get; set; } | Gets or sets the category of the document. |
| [Characters](characters) { get; set; } | Represents an estimate of the number of characters in the document. |
| [CharactersWithSpaces](characterswithspaces) { get; set; } | Represents an estimate of the number of characters (including spaces) in the document. |
| [Comments](comments) { get; set; } | Gets or sets the document comments. |
| [Company](company) { get; set; } | Gets or sets the company property. |
| [ContentStatus](contentstatus) { get; set; } | Gets or sets the ContentStatus of the document. |
| [ContentType](contenttype) { get; set; } | Gets or sets the ContentStatus of the document. |
| [CreatedTime](createdtime) { get; set; } | Gets or sets date of the document creation in UTC. |
| [HeadingPairs](headingpairs) { get; set; } | Specifies document headings and their names. |
| [HyperlinkBase](hyperlinkbase) { get; set; } | Specifies the base string used for evaluating relative hyperlinks in this document. |
| override [Item](item) { get; } | Returns a [`DocumentProperty`](../documentproperty) object by the name of the property. |
| [Keywords](keywords) { get; set; } | Gets or sets the document keywords. |
| [LastPrinted](lastprinted) { get; set; } | Gets or sets the date when the document was last printed in UTC. |
| [LastSavedBy](lastsavedby) { get; set; } | Gets or sets the name of the last author. |
| [LastSavedTime](lastsavedtime) { get; set; } | Gets or sets the time of the last save in UTC. |
| [Lines](lines) { get; set; } | Represents an estimate of the number of lines in the document. |
| [LinksUpToDate](linksuptodate) { get; set; } | Indicates whether hyperlinks in a document are up-to-date. |
| [Manager](manager) { get; set; } | Gets or sets the manager property. |
| [NameOfApplication](nameofapplication) { get; set; } | Gets or sets the name of the application. |
| [Pages](pages) { get; set; } | Represents an estimate of the number of pages in the document. |
| [Paragraphs](paragraphs) { get; set; } | Represents an estimate of the number of paragraphs in the document. |
| [RevisionNumber](revisionnumber) { get; set; } | Gets or sets the document revision number. |
| [Security](security) { get; set; } | Specifies the security level of a document as a numeric value. |
| [Subject](subject) { get; set; } | Gets or sets the subject of the document. |
| [Template](template) { get; set; } | Gets or sets the informational name of the document template. |
| [Thumbnail](thumbnail) { get; set; } | Gets or sets the thumbnail of the document. |
| [Title](title) { get; set; } | Gets or sets the title of the document. |
| [TitlesOfParts](titlesofparts) { get; set; } | Each string in the array specifies the name of a part in the document. |
| [TotalEditingTime](totaleditingtime) { get; set; } | Gets or sets the total editing time in minutes. |
| [Version](version) { get; set; } | Represents the version number of the application that created the document. |
| [Words](words) { get; set; } | Represents an estimate of the number of words in the document. |

### Remarks

Provides access to [`DocumentProperty`](../documentproperty) objects by their names (using an indexer) and via a set of typed properties that return values of appropriate types.

The names of the properties are case-insensitive.The properties in the collection are sorted alphabetically by name.

### Examples

Shows how to work with built-in document properties.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// The "Document" object contains some of its metadata in its members.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// The document also stores metadata in its built-in properties.
// Each built-in property is a member of the document's "BuiltInDocumentProperties" object.
Console.WriteLine("Built-in Properties:");
foreach (DocumentProperty docProperty in doc.BuiltInDocumentProperties)
{
    Console.WriteLine(docProperty.Name);
    Console.WriteLine($"\tType:\t{docProperty.Type}");

    // Some properties may store multiple values.
    if (docProperty.Value is ICollection<object>)
    {
        foreach (object value in docProperty.Value as ICollection<object>)
            Console.WriteLine($"\tValue:\t\"{value}\"");
    }
    else
    {
        Console.WriteLine($"\tValue:\t\"{docProperty.Value}\"");
    }
}
```

### See Also

* class [Document](../../aspose.words/document)
* property [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties)
* property [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties)
* class [DocumentPropertyCollection](../documentpropertycollection)
* namespace [Aspose.Words.Properties](../../aspose.words.properties)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

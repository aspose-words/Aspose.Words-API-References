---
title: BuiltInDocumentProperties
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 4150
url: /net/aspose.words.properties/builtindocumentproperties/
---
## BuiltInDocumentProperties class

A collection of built-in document properties.

```csharp
public class BuiltInDocumentProperties : DocumentPropertyCollection
```

## Properties

| Name | Description |
| --- | --- |
| [Author](../../aspose.words.properties/builtindocumentproperties/author) { get; set; } | Gets or sets the name of the document's author. |
| [Bytes](../../aspose.words.properties/builtindocumentproperties/bytes) { get; set; } | Represents an estimate of the number of bytes in the document. |
| [Category](../../aspose.words.properties/builtindocumentproperties/category) { get; set; } | Gets or sets the category of the document. |
| [Characters](../../aspose.words.properties/builtindocumentproperties/characters) { get; set; } | Represents an estimate of the number of characters in the document. |
| [CharactersWithSpaces](../../aspose.words.properties/builtindocumentproperties/characterswithspaces) { get; set; } | Represents an estimate of the number of characters (including spaces) in the document. |
| [Comments](../../aspose.words.properties/builtindocumentproperties/comments) { get; set; } | Gets or sets the document comments. |
| [Company](../../aspose.words.properties/builtindocumentproperties/company) { get; set; } | Gets or sets the company property. |
| [ContentStatus](../../aspose.words.properties/builtindocumentproperties/contentstatus) { get; set; } | Gets or sets the ContentStatus of the document. |
| [ContentType](../../aspose.words.properties/builtindocumentproperties/contenttype) { get; set; } | Gets or sets the ContentStatus of the document. |
| [Count](../../aspose.words.properties/documentpropertycollection/count) { get; } | Gets number of items in the collection. |
| [CreatedTime](../../aspose.words.properties/builtindocumentproperties/createdtime) { get; set; } | Gets or sets date of the document creation in UTC. |
| [HeadingPairs](../../aspose.words.properties/builtindocumentproperties/headingpairs) { get; set; } | Specifies document headings and their names. |
| [HyperlinkBase](../../aspose.words.properties/builtindocumentproperties/hyperlinkbase) { get; set; } | Specifies the base string used for evaluating relative hyperlinks in this document. |
| [Item](../../aspose.words.properties/documentpropertycollection/item) { get; } | Returns a [`DocumentProperty`](../documentproperty) object by index. |
| override [Item](../../aspose.words.properties/builtindocumentproperties/item) { get; } | Returns a [`DocumentProperty`](../documentproperty) object by the name of the property. |
| [Keywords](../../aspose.words.properties/builtindocumentproperties/keywords) { get; set; } | Gets or sets the document keywords. |
| [LastPrinted](../../aspose.words.properties/builtindocumentproperties/lastprinted) { get; set; } | Gets or sets the date when the document was last printed in UTC. |
| [LastSavedBy](../../aspose.words.properties/builtindocumentproperties/lastsavedby) { get; set; } | Gets or sets the name of the last author. |
| [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) { get; set; } | Gets or sets the time of the last save in UTC. |
| [Lines](../../aspose.words.properties/builtindocumentproperties/lines) { get; set; } | Represents an estimate of the number of lines in the document. |
| [LinksUpToDate](../../aspose.words.properties/builtindocumentproperties/linksuptodate) { get; set; } | Indicates whether hyperlinks in a document are up-to-date. |
| [Manager](../../aspose.words.properties/builtindocumentproperties/manager) { get; set; } | Gets or sets the manager property. |
| [NameOfApplication](../../aspose.words.properties/builtindocumentproperties/nameofapplication) { get; set; } | Gets or sets the name of the application. |
| [Pages](../../aspose.words.properties/builtindocumentproperties/pages) { get; set; } | Represents an estimate of the number of pages in the document. |
| [Paragraphs](../../aspose.words.properties/builtindocumentproperties/paragraphs) { get; set; } | Represents an estimate of the number of paragraphs in the document. |
| [RevisionNumber](../../aspose.words.properties/builtindocumentproperties/revisionnumber) { get; set; } | Gets or sets the document revision number. |
| [Security](../../aspose.words.properties/builtindocumentproperties/security) { get; set; } | Specifies the security level of a document as a numeric value. |
| [Subject](../../aspose.words.properties/builtindocumentproperties/subject) { get; set; } | Gets or sets the subject of the document. |
| [Template](../../aspose.words.properties/builtindocumentproperties/template) { get; set; } | Gets or sets the informational name of the document template. |
| [Thumbnail](../../aspose.words.properties/builtindocumentproperties/thumbnail) { get; set; } | Gets or sets the thumbnail of the document. |
| [Title](../../aspose.words.properties/builtindocumentproperties/title) { get; set; } | Gets or sets the title of the document. |
| [TitlesOfParts](../../aspose.words.properties/builtindocumentproperties/titlesofparts) { get; set; } | Each string in the array specifies the name of a part in the document. |
| [TotalEditingTime](../../aspose.words.properties/builtindocumentproperties/totaleditingtime) { get; set; } | Gets or sets the total editing time in minutes. |
| [Version](../../aspose.words.properties/builtindocumentproperties/version) { get; set; } | Represents the version number of the application that created the document. |
| [Words](../../aspose.words.properties/builtindocumentproperties/words) { get; set; } | Represents an estimate of the number of words in the document. |

## Methods

| Name | Description |
| --- | --- |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear)() | Removes all properties from the collection. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains)(string) | Returns true if a property with the specified name exists in the collection. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator)() | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof)(string) | Gets the index of a property by name. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove)(string) | Removes a property with the specified name from the collection. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat)(int) | Removes a property at the specified index. |

### Remarks

Provides access to [`DocumentProperty`](../documentproperty) objects by their names (using an indexer) and via a set of typed properties that return values of appropriate types.

The names of the properties are case-insensitive.

The properties in the collection are sorted alphabetically by name.

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

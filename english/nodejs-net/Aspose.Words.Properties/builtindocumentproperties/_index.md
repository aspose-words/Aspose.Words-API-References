---
title: BuiltInDocumentProperties class
linktitle: BuiltInDocumentProperties class
articleTitle: BuiltInDocumentProperties class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Properties.BuiltInDocumentProperties class. A collection of built-in document properties"
type: docs
weight: 10
url: /nodejs-net/aspose.words.properties/builtindocumentproperties/
---

## BuiltInDocumentProperties class

A collection of built-in document properties.
To learn more, visit the [Work with Document Properties](https://docs.aspose.com/words/nodejs-net/work-with-document-properties/) documentation article.




### Remarks

Provides access to [DocumentProperty](../documentproperty/) objects by their names (using an indexer) and
via a set of typed properties that return values of appropriate types.




The names of the properties are case-insensitive.

The properties in the collection are sorted alphabetically by name.




**Inheritance:** [BuiltInDocumentProperties](./) → [DocumentPropertyCollection](../documentpropertycollection/)

### Properties

| Name | Description |
| --- | --- |
| [author](./author/) | Gets or sets the name of the document's author. |
| [bytes](./bytes/) | Represents an estimate of the number of bytes in the document. |
| [category](./category/) | Gets or sets the category of the document. |
| [characters](./characters/) | Represents an estimate of the number of characters in the document. |
| [charactersWithSpaces](./charactersWithSpaces/) | Represents an estimate of the number of characters (including spaces) in the document. |
| [comments](./comments/) | Gets or sets the document comments. |
| [company](./company/) | Gets or sets the company property. |
| [contentStatus](./contentStatus/) | Gets or sets the content status of the document. |
| [contentType](./contentType/) | Gets or sets the content type of the document. |
| [count](../documentpropertycollection/count/) | Gets number of items in the collection.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
| [createdTime](./createdTime/) | Gets or sets date of the document creation in UTC. |
| [hyperlinkBase](./hyperlinkBase/) | Specifies the base string used for evaluating relative hyperlinks in this document. |
| [hyperlinksChanged](./hyperlinksChanged/) | Indicates whether hyperlinks in a document were changed. |
| [keywords](./keywords/) | Gets or sets the document keywords. |
| [lastPrinted](./lastPrinted/) | Gets or sets the date when the document was last printed in UTC. |
| [lastSavedBy](./lastSavedBy/) | Gets or sets the name of the last author. |
| [lastSavedTime](./lastSavedTime/) | Gets or sets the time of the last save in UTC. |
| [lines](./lines/) | Represents an estimate of the number of lines in the document. |
| [linksUpToDate](./linksUpToDate/) | Indicates whether hyperlinks in a document are up-to-date. |
| [manager](./manager/) | Gets or sets the manager property. |
| [nameOfApplication](./nameOfApplication/) | Gets or sets the name of the application. |
| [pages](./pages/) | Represents an estimate of the number of pages in the document. |
| [paragraphs](./paragraphs/) | Represents an estimate of the number of paragraphs in the document. |
| [revisionNumber](./revisionNumber/) | Gets or sets the document revision number. |
| [scaleCrop](./scaleCrop/) | Indicates whether document thumbnail is cropped or scaled to fit the display. |
| [security](./security/) | Specifies the security level of a document as a numeric value. |
| [sharedDocument](./sharedDocument/) | Indicates whether the document is a shared document. |
| [subject](./subject/) | Gets or sets the subject of the document. |
| [template](./template/) | Gets or sets the informational name of the document template. |
| [this[]](../documentpropertycollection/this[]/) | <br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
| [this[]](../documentpropertycollection/this[]/) | <br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
| [thumbnail](./thumbnail/) | Gets or sets the thumbnail of the document. |
| [title](./title/) | Gets or sets the title of the document. |
| [titlesOfParts](./titlesOfParts/) | Each string in the array specifies the name of a part in the document. |
| [totalEditingTime](./totalEditingTime/) | Gets or sets the total editing time in minutes. |
| [version](./version/) | Represents the version number of the application that created the document. |
| [words](./words/) | Represents an estimate of the number of words in the document. |

### Methods

| Name | Description |
| --- | --- |
|[ clear()](../documentpropertycollection/clear/#default) | Removes all properties from the collection.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
|[ contains(name)](../documentpropertycollection/contains/#string) | Returns ``true`` if a property with the specified name exists in the collection.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
|[ indexOf(name)](../documentpropertycollection/indexOf/#string) | Gets the index of a property by name.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
|[ remove(name)](../documentpropertycollection/remove/#string) | Removes a property with the specified name from the collection.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
|[ removeAt(index)](../documentpropertycollection/removeAt/#number) | Removes a property at the specified index.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |

### Examples

Shows how to work with built-in document properties.

```js
let doc = new aw.Document(base.myDir + "Properties.docx");

// The "Document" object contains some of its metadata in its members.
//console.log(`Document filename:\n\t \"${doc.originalFileName}\"`);

// The document also stores metadata in its built-in properties.
// Each built-in property is a member of the document's "BuiltInDocumentProperties" object.
/*console.log("Built-in Properties:");
for (let docProperty of doc.builtInDocumentProperties)
{
  console.log(docProperty.name);
  console.log(`\tType:\t${docProperty.type}`);
  console.log(`\tValue:\t\"${docProperty.toString()}\"`);
}*/
```

### See Also

* module [Aspose.Words.Properties](../)
* class [DocumentPropertyCollection](../documentpropertycollection/)
* class [Document](../../aspose.words/document/)
* property [Document.builtInDocumentProperties](../../aspose.words/document/builtInDocumentProperties/)
* property [Document.customDocumentProperties](../../aspose.words/document/customDocumentProperties/)


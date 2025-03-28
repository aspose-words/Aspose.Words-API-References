---
title: BuiltInDocumentProperties.Keywords
linktitle: Keywords
articleTitle: Keywords
second_title: Aspose.Words for .NET
description: Enhance your documents with BuiltInDocumentProperties. Easily manage keywords to improve searchability and organization for better productivity.
type: docs
weight: 150
url: /net/aspose.words.properties/builtindocumentproperties/keywords/
---
## BuiltInDocumentProperties.Keywords property

Gets or sets the document keywords.

```csharp
public string Keywords { get; set; }
```

## Examples

Shows how to work with built-in document properties in the "Description" category.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Below are four built-in document properties that have fields that can display their values in the document body.
// 1 -  "Author" property, which we can display using an AUTHOR field:
properties.Author = "John Doe";
builder.Write("Author:\t");
builder.InsertField(FieldType.FieldAuthor, true);

// 2 -  "Title" property, which we can display using a TITLE field:
properties.Title = "John's Document";
builder.Write("\nDoc title:\t");
builder.InsertField(FieldType.FieldTitle, true);

// 3 -  "Subject" property, which we can display using a SUBJECT field:
properties.Subject = "My subject";
builder.Write("\nSubject:\t");
builder.InsertField(FieldType.FieldSubject, true);

// 4 -  "Comments" property, which we can display using a COMMENTS field:
properties.Comments = $"This is {properties.Author}'s document about {properties.Subject}";
builder.Write("\nComments:\t\"");
builder.InsertField(FieldType.FieldComments, true);
builder.Write("\"");

// The "Category" built-in property does not have a field that can display its value.
properties.Category = "My category";

// We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
properties.Keywords = "Tag 1; Tag 2; Tag 3";

// We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
// The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
doc.Save(ArtifactsDir + "DocumentProperties.Description.docx");
```

### See Also

* class [BuiltInDocumentProperties](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)

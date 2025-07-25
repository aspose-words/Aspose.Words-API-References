---
title: FieldAuthor.AuthorName
linktitle: AuthorName
articleTitle: AuthorName
second_title: Aspose.Words for .NET
description: Manage document authors effortlessly with FieldAuthor AuthorName. Easily get or set author names to enhance your content's credibility and organization.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldauthor/authorname/
---
## FieldAuthor.AuthorName property

Gets or sets the document author's name.

```csharp
public string AuthorName { get; set; }
```

## Examples

Shows how to use an AUTHOR field to display a document creator's name.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// AUTHOR fields source their results from the built-in document property called "Author".
// If we create and save a document in Microsoft Word,
// it will have our username in that property.
// However, if we create a document programmatically using Aspose.Words,
// the "Author" property, by default, will be an empty string. 
Assert.That(doc.BuiltInDocumentProperties.Author, Is.EqualTo(string.Empty));

// Set a backup author name for AUTHOR fields to use
// if the "Author" property contains an empty string.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo(" AUTHOR "));
Assert.That(field.Result, Is.EqualTo("Joe Bloggs"));

// Updating an AUTHOR field that contains a value
// will apply that value to the "Author" built-in property.
Assert.That(doc.BuiltInDocumentProperties.Author, Is.EqualTo("Joe Bloggs"));

// Changing this property, then updating the AUTHOR field will apply this value to the field.
doc.BuiltInDocumentProperties.Author = "John Doe";
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo(" AUTHOR "));
Assert.That(field.Result, Is.EqualTo("John Doe"));

// If we update an AUTHOR field after changing its "Name" property,
// then the field will display the new name and apply the new name to the built-in property.
field.AuthorName = "Jane Doe";
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo(" AUTHOR  \"Jane Doe\""));
Assert.That(field.Result, Is.EqualTo("Jane Doe"));

// AUTHOR fields do not affect the DefaultDocumentAuthor property.
Assert.That(doc.BuiltInDocumentProperties.Author, Is.EqualTo("Jane Doe"));
Assert.That(doc.FieldOptions.DefaultDocumentAuthor, Is.EqualTo("Joe Bloggs"));

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### See Also

* class [FieldAuthor](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)

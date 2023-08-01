---
title: FieldOptions.DefaultDocumentAuthor
linktitle: DefaultDocumentAuthor
articleTitle: DefaultDocumentAuthor
second_title: Aspose.Words for .NET
description: FieldOptions DefaultDocumentAuthor property. Gets or sets default document authors name. If authors name is already specified in builtin document properties this option is not considered in C#.
type: docs
weight: 70
url: /net/aspose.words.fields/fieldoptions/defaultdocumentauthor/
---
## FieldOptions.DefaultDocumentAuthor property

Gets or sets default document author's name. If author's name is already specified in built-in document properties, this option is not considered.

```csharp
public string DefaultDocumentAuthor { get; set; }
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
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// Set a backup author name for AUTHOR fields to use
// if the "Author" property contains an empty string.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// Updating an AUTHOR field that contains a value
// will apply that value to the "Author" built-in property.
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// Changing this property, then updating the AUTHOR field will apply this value to the field.
doc.BuiltInDocumentProperties.Author = "John Doe";      
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// If we update an AUTHOR field after changing its "Name" property,
// then the field will display the new name and apply the new name to the built-in property.
field.AuthorName = "Jane Doe";
field.Update();

Assert.AreEqual(" AUTHOR  \"Jane Doe\"", field.GetFieldCode());
Assert.AreEqual("Jane Doe", field.Result);

// AUTHOR fields do not affect the DefaultDocumentAuthor property.
Assert.AreEqual("Jane Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Joe Bloggs", doc.FieldOptions.DefaultDocumentAuthor);

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### See Also

* class [FieldOptions](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)

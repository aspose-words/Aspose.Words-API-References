---
title: FieldOptions.DefaultDocumentAuthor
linktitle: DefaultDocumentAuthor
articleTitle: DefaultDocumentAuthor
second_title: Aspose.Words för .NET
description: Hantera egenskapen DefaultDocumentAuthor för att enkelt ange eller uppdatera dokumentförfattarnas namn, vilket förbättrar organisationen och effektiviteten i dokumenthanteringen.
type: docs
weight: 70
url: /sv/net/aspose.words.fields/fieldoptions/defaultdocumentauthor/
---
## FieldOptions.DefaultDocumentAuthor property

Hämtar eller anger standardnamnet på dokumentförfattaren. Om författarnamnet redan är angett i de inbyggda dokumentegenskaperna, beaktas inte det här alternativet.

```csharp
public string DefaultDocumentAuthor { get; set; }
```

## Exempel

Visar hur man använder ett AUTHOR-fält för att visa namnet på en dokumentskapare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// AUTHOR-fält hämtar sina resultat från den inbyggda dokumentegenskapen som heter "Author".
// Om vi skapar och sparar ett dokument i Microsoft Word,
// den kommer att ha vårt användarnamn i den egenskapen.
// Men om vi skapar ett dokument programmatiskt med Aspose.Words,
// egenskapen "Author" kommer som standard att vara en tom sträng.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// Ange ett reservförfattarnamn för AUTHOR-fält att använda
// om egenskapen "Author" innehåller en tom sträng.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// Uppdaterar ett AUTHOR-fält som innehåller ett värde
// kommer att tillämpa det värdet på den inbyggda egenskapen "Author".
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// Om du ändrar den här egenskapen och sedan uppdaterar fältet AUTHOR tillämpas det här värdet på fältet.
doc.BuiltInDocumentProperties.Author = "John Doe";
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// Om vi uppdaterar ett AUTHOR-fält efter att ha ändrat dess "Name"-egenskap,
// då visar fältet det nya namnet och tillämpar det nya namnet på den inbyggda egenskapen.
field.AuthorName = "Jane Doe";
field.Update();

Assert.AreEqual(" AUTHOR  \"Jane Doe\"", field.GetFieldCode());
Assert.AreEqual("Jane Doe", field.Result);

// AUTHOR-fält påverkar inte egenskapen DefaultDocumentAuthor.
Assert.AreEqual("Jane Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Joe Bloggs", doc.FieldOptions.DefaultDocumentAuthor);

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### Se även

* class [FieldOptions](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)

---
title: FieldAuthor.AuthorName
linktitle: AuthorName
articleTitle: AuthorName
second_title: Aspose.Words för .NET
description: Hantera dokumentförfattare enkelt med FieldAuthor AuthorName. Hämta eller ange enkelt författarnamn för att förbättra ditt innehålls trovärdighet och organisation.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldauthor/authorname/
---
## FieldAuthor.AuthorName property

Hämtar eller anger dokumentförfattarens namn.

```csharp
public string AuthorName { get; set; }
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

* class [FieldAuthor](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)

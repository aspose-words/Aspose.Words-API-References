---
title: FieldOptions.DefaultDocumentAuthor
second_title: Aspose.Words för .NET API Referens
description: FieldOptions fast egendom. Hämtar eller ställer in standarddokumentets författares namn. Om författarens namn redan är specificerat i inbyggda dokumentegenskaper övervägs inte detta alternativ.
type: docs
weight: 70
url: /sv/net/aspose.words.fields/fieldoptions/defaultdocumentauthor/
---
## FieldOptions.DefaultDocumentAuthor property

Hämtar eller ställer in standarddokumentets författares namn. Om författarens namn redan är specificerat i inbyggda dokumentegenskaper, övervägs inte detta alternativ.

```csharp
public string DefaultDocumentAuthor { get; set; }
```

### Exempel

Visar hur man använder ett AUTHOR-fält för att visa en dokumentskapares namn.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// AUTHOR-fält hämtar sina resultat från den inbyggda dokumentegenskapen som kallas "Author".
// Om vi skapar och sparar ett dokument i Microsoft Word,
// det kommer att ha vårt användarnamn i den egenskapen.
// Men om vi skapar ett dokument programmatiskt med Aspose.Words,
// egenskapen "Author" kommer som standard att vara en tom sträng.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// Ställ in ett säkerhetskopieringsförfattarnamn för AUTHOR-fält att använda
// om egenskapen "Author" innehåller en tom sträng.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// Uppdatering av ett AUTHOR-fält som innehåller ett värde
// kommer att tillämpa det värdet på den inbyggda egenskapen "Author".
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// Om du ändrar den här egenskapen och sedan uppdaterar fältet AUTHOR kommer detta värde att tillämpas på fältet.
doc.BuiltInDocumentProperties.Author = "John Doe";      
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// Om vi uppdaterar ett AUTHOR-fält efter att ha ändrat dess "Name"-egenskap,
// då kommer fältet att visa det nya namnet och tillämpa det nya namnet på den inbyggda egenskapen.
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
* namnutrymme [Aspose.Words.Fields](../../fieldoptions/)
* hopsättning [Aspose.Words](../../../)



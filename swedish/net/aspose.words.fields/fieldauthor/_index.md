---
title: FieldAuthor
second_title: Aspose.Words för .NET API Referens
description: Implementerar fältet AUTHOR.
type: docs
weight: 1420
url: /sv/net/aspose.words.fields/fieldauthor/
---
## FieldAuthor class

Implementerar fältet AUTHOR.

```csharp
public class FieldAuthor : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldAuthor](fieldauthor)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AuthorName](../../aspose.words.fields/fieldauthor/authorname) { get; set; } | Hämtar eller ställer in dokumentets författares namn. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end) { get; } | Hämtar noden som representerar fältänden. |
| [Format](../../aspose.words.fields/field/format) { get; } | Får en[`FieldFormat`](../fieldformat) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara null. |
| [Start](../../aspose.words.fields/field/start) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras **null** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update)(bool) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

### Anmärkningar

Hämtar och ställer eventuellt in dokumentförfattarens namn, som registrerats i **Författare**egenskapen för inbyggda dokumentegenskaper.

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

* class [Field](../field)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

---
title: FieldAuthor Class
linktitle: FieldAuthor
articleTitle: FieldAuthor
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldAuthor, utformad för att enkelt implementera AUTHOR-fältet för förbättrad dokumenthantering och automatisering.
type: docs
weight: 1980
url: /sv/net/aspose.words.fields/fieldauthor/
---
## FieldAuthor class

Implementerar AUTHOR-fältet.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldAuthor : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldAuthor](fieldauthor/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AuthorName](../../aspose.words.fields/fieldauthor/authorname/) { get; set; } | Hämtar eller anger dokumentförfattarens namn. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller anger text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista undernoden till dess överordnade nod, returneras dess överordnade stycke. Om fältet redan är borttaget returneras`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavkopplingen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Körs om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Utför en fältuppdatering. Körs om fältet redan uppdateras. |

## Anmärkningar

Hämtar, och anger valfritt, dokumentförfattarens namn, så som det är registrerat i**Författare** egenskapen för de inbyggda dokumentegenskaperna .

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

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)

---
title: FieldStyleRef.SuppressNonDelimiters
linktitle: SuppressNonDelimiters
articleTitle: SuppressNonDelimiters
second_title: Aspose.Words för .NET
description: Kontrollera icke-avgränsande tecken med egenskapen FieldStyleRef SuppressNonDelimiters. Förbättra datatydlighet och presentation i dina applikationer.
type: docs
weight: 80
url: /sv/net/aspose.words.fields/fieldstyleref/suppressnondelimiters/
---
## FieldStyleRef.SuppressNonDelimiters property

Hämtar eller anger om icke-avgränsande tecken ska undertryckas.

```csharp
public bool SuppressNonDelimiters { get; set; }
```

## Exempel

Visar hur man använder STYLEREF-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa en lista baserad på en listmall i Microsoft Word.
Aspose.Words.Lists.List list = doc.Lists.Add(Aspose.Words.Lists.ListTemplate.NumberDefault);

// Den här genererade listan kommer att visa "1.a)".
 // Mellanslag före parentesen är ett icke-avgränsande tecken, vilket vi kan undertrycka.
list.ListLevels[0].NumberFormat = "\x0000.";
list.ListLevels[1].NumberFormat = "\x0001 )";

// Lägg till text och använd styckeformat som STYLEREF-fält refererar till.
builder.ListFormat.List = list;
builder.ListFormat.ListIndent();
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 1");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln("Item 2");
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 3");
builder.ListFormat.RemoveNumbers();
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Placera ett STYLEREF-fält i sidhuvudet och visa den första texten i dokumentet med "List Paragraph"-formatering.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
FieldStyleRef field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";

// Placera ett STYLEREF-fält i sidfoten och låt det visa den sista texten.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";
field.SearchFromBottom = true;

builder.MoveToDocumentEnd();

// Vi kan också använda STYLEREF-fält för att referera till listnumren för listor.
builder.Write("\nParagraph number: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumber = true;

builder.Write("\nParagraph number, relative context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInRelativeContext = true;

builder.Write("\nParagraph number, full context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;

builder.Write("\nParagraph number, full context, non-delimiter chars suppressed: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;
field.SuppressNonDelimiters = true;

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.STYLEREF.docx");
```

### Se även

* class [FieldStyleRef](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)

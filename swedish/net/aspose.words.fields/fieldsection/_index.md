---
title: FieldSection
second_title: Aspose.Words för .NET API Referens
description: Implementerar fältet SECTION.
type: docs
weight: 2210
url: /sv/net/aspose.words.fields/fieldsection/
---
## FieldSection class

Implementerar fältet SECTION.

```csharp
public class FieldSection : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldSection](fieldsection/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältänden. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara null. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras **null** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

### Anmärkningar

Hämtar numret på den aktuella sektionen.

### Exempel

Visar hur du använder fälten SECTION och SECTIONPAGES för att numrera sidor efter sektioner.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;

// Ett SECTION-fält visar numret på sektionen det är i.
builder.Write("Section ");
FieldSection fieldSection = (FieldSection)builder.InsertField(FieldType.FieldSection, true);

Assert.AreEqual(" SECTION ", fieldSection.GetFieldCode());

// Ett PAGE-fält visar numret på sidan den är på.
builder.Write("\nPage ");
FieldPage fieldPage = (FieldPage)builder.InsertField(FieldType.FieldPage, true);

Assert.AreEqual(" PAGE ", fieldPage.GetFieldCode());

// Ett SECTIONPAGES-fält visar antalet sidor som avsnittet det är i sträcker sig över.
builder.Write(" of ");
FieldSectionPages fieldSectionPages = (FieldSectionPages)builder.InsertField(FieldType.FieldSectionPages, true);

Assert.AreEqual(" SECTIONPAGES ", fieldSectionPages.GetFieldCode());

// Flytta tillbaka från sidhuvudet till huvuddokumentet och infoga två sidor.
// Alla dessa sidor kommer att finnas i det första avsnittet. Våra fält, som visas en gång varje rubrik,
// kommer att numrera de aktuella/totala sidorna i detta avsnitt.
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Vi kan infoga ett nytt avsnitt med dokumentbyggaren så här.
// Detta kommer att påverka värdena som visas i fälten SECTION och SECTIONPAGES i alla kommande rubriker.
builder.InsertBreak(BreakType.SectionBreakNewPage);

// PAGE-fältet fortsätter att räkna sidor i hela dokumentet.
// Vi kan manuellt återställa antalet vid varje avsnitt för att hålla reda på sidor avsnitt för avsnitt.
builder.CurrentSection.PageSetup.RestartPageNumbering = true;
builder.InsertBreak(BreakType.PageBreak);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SECTION.SECTIONPAGES.docx");
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

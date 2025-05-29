---
title: FieldCitation Class
linktitle: FieldCitation
articleTitle: FieldCitation
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldCitation för smidig citeringshantering i dokument. Förbättra ditt skrivande med effektiv fältimplementering!
type: docs
weight: 2090
url: /sv/net/aspose.words.fields/fieldcitation/
---
## FieldCitation class

Implementerar CITATION-fältet.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldCitation : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldCitation](fieldcitation/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AnotherSourceTag](../../aspose.words.fields/fieldcitation/anothersourcetag/) { get; set; } | Hämtar eller ställer in ett värde som matchar**Märka** elementets värde från en annan källa som ska inkluderas i hänvisningen. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [FormatLanguageId](../../aspose.words.fields/fieldcitation/formatlanguageid/) { get; set; } | Hämtar eller anger språk-ID:t som används tillsammans med den angivna bibliografiska stilen för att formatera hänvisningen i dokumentet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [PageNumber](../../aspose.words.fields/fieldcitation/pagenumber/) { get; set; } | Hämtar eller anger ett sidnummer associerat med hänvisningen. |
| [Prefix](../../aspose.words.fields/fieldcitation/prefix/) { get; set; } | Hämtar eller anger ett prefix som läggs till före hänvisningen. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller anger text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [SourceTag](../../aspose.words.fields/fieldcitation/sourcetag/) { get; set; } | Hämtar eller ställer in ett värde som matchar**Märka** elementets värde för källan som ska infogas. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| [Suffix](../../aspose.words.fields/fieldcitation/suffix/) { get; set; } | Hämtar eller anger ett suffix som läggs till i hänvisningen. |
| [SuppressAuthor](../../aspose.words.fields/fieldcitation/suppressauthor/) { get; set; } | Hämtar eller anger om författarinformationen ska utelämnas från citeringen. |
| [SuppressTitle](../../aspose.words.fields/fieldcitation/suppresstitle/) { get; set; } | Hämtar eller anger om titelinformationen ska utelämnas från hänvisningen. |
| [SuppressYear](../../aspose.words.fields/fieldcitation/suppressyear/) { get; set; } | Hämtar eller anger om årsinformationen ska utelämnas från hänvisningen. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |
| [VolumeNumber](../../aspose.words.fields/fieldcitation/volumenumber/) { get; set; } | Hämtar eller ställer in ett volymnummer associerat med hänvisningen. |

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

Infogar innehållet i**Källa** element med ett specificerat**Märka** element med hjälp av en bibliografisk stil.

## Exempel

Visar hur man arbetar med fälten CITATION och BIBLIOGRAFI.

```csharp
// Öppna ett dokument som innehåller bibliografiska källor som vi kan hitta i
// Microsoft Word via referenser -> Citat och bibliografi -> Hantera källor.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Skapa en hänvisning med bara sidnumret och författaren till den refererade boken.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Vi hänvisar till källor med hjälp av deras taggnamn.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// Skapa en mer detaljerad hänvisning som citerar två källor.
builder.InsertParagraph();
builder.Write("Text to be cited with two sources.");
fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);
fieldCitation.SourceTag = "Book1";
fieldCitation.AnotherSourceTag = "Book2";
fieldCitation.FormatLanguageId = "en-US";
fieldCitation.PageNumber = "19";
fieldCitation.Prefix = "Prefix ";
fieldCitation.Suffix = " Suffix";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = false;
fieldCitation.SuppressYear = false;
fieldCitation.VolumeNumber = "VII";

Assert.AreEqual(" CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f \"Prefix \" \\s \" Suffix\" \\v VII", fieldCitation.GetFieldCode());

// Vi kan använda ett fält för BIBLIOGRAFI för att visa alla källor i dokumentet.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "5129";
fieldBibliography.FilterLanguageId = "5129";
fieldBibliography.SourceTag = "Book2";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129 \\f 5129 \\m Book2", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)

---
title: FieldIncludeText Class
linktitle: FieldIncludeText
articleTitle: FieldIncludeText
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldIncludeText för sömlös dokumentintegration. Förbättra ditt arbetsflöde med effektiv implementering av INCLUDETEXT-fält.
type: docs
weight: 2460
url: /sv/net/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class

Implementerar INCLUDETEXT-fältet.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldIncludeText : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldIncludeText](fieldincludetext/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldincludetext/bookmarkname/) { get; set; } | Hämtar eller ställer in namnet på bokmärket i dokumentet som ska inkluderas. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [Encoding](../../aspose.words.fields/fieldincludetext/encoding/) { get; set; } | Hämtar eller ställer in kodningen som tillämpas på data i den refererade filen. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [LockFields](../../aspose.words.fields/fieldincludetext/lockfields/) { get; set; } | Hämtar eller anger om fält i det inkluderade dokumentet ska förhindras från att uppdateras. |
| [MimeType](../../aspose.words.fields/fieldincludetext/mimetype/) { get; set; } | Hämtar eller ställer in MIME-typen för den refererade filen. |
| [NamespaceMappings](../../aspose.words.fields/fieldincludetext/namespacemappings/) { get; set; } | Hämtar eller ställer in namnrymdsmappningar för XPath-frågor. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller anger text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [SourceFullName](../../aspose.words.fields/fieldincludetext/sourcefullname/) { get; set; } | Hämtar eller anger dokumentets plats med hjälp av en IRI. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| [TextConverter](../../aspose.words.fields/fieldincludetext/textconverter/) { get; set; } | Hämtar eller anger namnet på textkonverteraren för formatet för den inkluderade filen. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |
| [XPath](../../aspose.words.fields/fieldincludetext/xpath/) { get; set; } | Hämtar eller ställer in XPath för önskad del av XML-filen. |
| [XslTransformation](../../aspose.words.fields/fieldincludetext/xsltransformation/) { get; set; } | Hämtar eller anger platsen för XSL-transformationen för att formatera XML-data. |

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

Infogar hela eller delar av texten och bilderna som finns i ett annat dokument.

## Exempel

Visar hur man skapar ett INCLUDETEXT-fält och anger dess egenskaper.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Nedan följer två sätt att använda INCLUDETEXT-fält för att visa innehållet i en XML-fil i det lokala filsystemet.
    // 1 - Utför en XSL-transformation på ett XML-dokument:
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2 - Använd en XPath för att hämta specifika element från ett XML-dokument:
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");
}

/// <summary>
/// Använd en dokumentbyggare för att infoga ett INCLUDETEXT-fält med anpassade egenskaper.
/// </summary>
public FieldIncludeText CreateFieldIncludeText(DocumentBuilder builder, string sourceFullName, bool lockFields, string mimeType, string textConverter, string encoding)
{
    FieldIncludeText fieldIncludeText = (FieldIncludeText)builder.InsertField(FieldType.FieldIncludeText, true);
    fieldIncludeText.SourceFullName = sourceFullName;
    fieldIncludeText.LockFields = lockFields;
    fieldIncludeText.MimeType = mimeType;
    fieldIncludeText.TextConverter = textConverter;
    fieldIncludeText.Encoding = encoding;

    return fieldIncludeText;
}
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)

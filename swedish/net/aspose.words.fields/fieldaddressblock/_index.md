---
title: FieldAddressBlock Class
linktitle: FieldAddressBlock
articleTitle: FieldAddressBlock
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldAddressBlock för sömlös integration av ADDRESSBLOCK-fält i dina dokument. Förbättra din dokumentautomation idag!
type: docs
weight: 1940
url: /sv/net/aspose.words.fields/fieldaddressblock/
---
## FieldAddressBlock class

Implementerar ADRESSBLOCK-fältet.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldAddressBlock : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldAddressBlock](fieldaddressblock/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [ExcludedCountryOrRegionName](../../aspose.words.fields/fieldaddressblock/excludedcountryorregionname/) { get; set; } | Hämtar eller anger namnet på det undantagna landet/regionen. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [FormatAddressOnCountryOrRegion](../../aspose.words.fields/fieldaddressblock/formataddressoncountryorregion/) { get; set; } | Hämtar eller anger om adressen ska formateras enligt mottagarens land/region enligt definitionen i POST*CODE (Universal Postal Union 2006). |
| [IncludeCountryOrRegionName](../../aspose.words.fields/fieldaddressblock/includecountryorregionname/) { get; set; } | Hämtar eller anger om namnet på landet/regionen ska inkluderas. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [LanguageId](../../aspose.words.fields/fieldaddressblock/languageid/) { get; set; } | Hämtar eller anger språk-ID:t som används för att formatera adressen. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [NameAndAddressFormat](../../aspose.words.fields/fieldaddressblock/nameandaddressformat/) { get; set; } | Hämtar eller ställer in namn- och adressformatet. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller anger text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [GetFieldNames](../../aspose.words.fields/fieldaddressblock/getfieldnames/)() | Returnerar en samling namn på fält för kopplingsmeddelanden som används av fältet. |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista undernoden till dess överordnade nod, returneras dess överordnade stycke. Om fältet redan är borttaget returneras`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavkopplingen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Körs om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Utför en fältuppdatering. Körs om fältet redan uppdateras. |

## Anmärkningar

Representerar ett adressblock. Enadressblock är ett textblock som anger information som är lämplig för en postadress, i den ordning som destinationslandet kräver.

## Exempel

Visar hur man hämtar fältnamn för dokumentkoppling som används av ett fält.

```csharp
Document doc = new Document(MyDir + "Field sample - ADDRESSBLOCK.docx");

string[] addressFieldsExpect =
{
    "Company", "First Name", "Middle Name", "Last Name", "Suffix", "Address 1", "City", "State",
    "Country or Region", "Postal Code"
};

FieldAddressBlock addressBlockField = (FieldAddressBlock) doc.Range.Fields[0];
string[] addressBlockFieldNames = addressBlockField.GetFieldNames();
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)

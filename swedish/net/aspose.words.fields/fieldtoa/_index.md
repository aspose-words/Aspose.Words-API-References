---
title: FieldToa Class
linktitle: FieldToa
articleTitle: FieldToa
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldToa för sömlös implementering av TOA-fält. Förbättra din dokumenthantering med kraftfulla funktioner idag!
type: docs
weight: 2930
url: /sv/net/aspose.words.fields/fieldtoa/
---
## FieldToa class

Implementerar TOA-fältet.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldToa : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldToa](fieldtoa/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoa/bookmarkname/) { get; set; } | Hämtar eller anger namnet på bokmärket som markerar den del av dokumentet som används för att bygga tabellen. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [EntryCategory](../../aspose.words.fields/fieldtoa/entrycategory/) { get; set; } | Hämtar eller ställer in integralkategorin för poster som ingår i tabellen. |
| [EntrySeparator](../../aspose.words.fields/fieldtoa/entryseparator/) { get; set; } | Hämtar eller anger teckensekvensen som används för att separera en post i en auktoritetsförteckning och dess sidnummer. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldtoa/pagenumberlistseparator/) { get; set; } | Hämtar eller anger teckensekvensen som används för att separera två sidnummer i en sidnummerlista. |
| [PageRangeSeparator](../../aspose.words.fields/fieldtoa/pagerangeseparator/) { get; set; } | Hämtar eller anger teckensekvensen som används för att separera början och slutet av ett sidintervall. |
| [RemoveEntryFormatting](../../aspose.words.fields/fieldtoa/removeentryformatting/) { get; set; } | Hämtar eller anger om formateringen av posttexten i dokumentet ska tas bort från posten i auktoritetstabellen. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller anger text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [SequenceName](../../aspose.words.fields/fieldtoa/sequencename/) { get; set; } | Hämtar eller anger namnet på en sekvens vars nummer ingår i sidnumret. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoa/sequenceseparator/) { get; set; } | Hämtar eller anger teckensekvensen som används för att separera sekvensnummer och sidnummer. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |
| [UseHeading](../../aspose.words.fields/fieldtoa/useheading/) { get; set; } | Hämtar eller anger om kategorirubriken ska inkluderas för posterna i en auktoritetstabell. |
| [UsePassim](../../aspose.words.fields/fieldtoa/usepassim/) { get; set; } | Hämtar eller anger om fem eller fler olika sidreferenser till samma auktoritet ska ersättas med "passim", vilket används för att indikera att ett ord eller ett avsnitt förekommer ofta i det citerade verket. |

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

Skapar en auktoritetstabell (det vill säga en lista över referenser i ett juridiskt dokument, såsom referenser till rättsfall, stadgar och regler, tillsammans med numren på de sidor där referenserna visas) med hjälp av de poster som anges av TA-fälten.

## Exempel

Visar hur man skapar och anpassar en auktoritetstabell med hjälp av fälten TOA och TA.

```csharp
public void FieldTOA()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Infoga ett TOA-fält, vilket skapar en post för varje TA-fält i dokumentet,
    // visar långa hänvisningar och sidnummer för varje post.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // Ange postkategori för vår tabell. Denna användarvillkorsbeskrivning (TOA) kommer nu endast att inkludera TA-fält
    // som har ett matchande värde i sin EntryCategory-egenskap.
    fieldToa.EntryCategory = "1";

    // Dessutom är kategorin "Tabell över auktoriteter" vid index 1 "Fall",
    // som kommer att visas som vår tabells titel om vi ställer in variabeln till true.
    fieldToa.UseHeading = true;

    // Vi kan ytterligare filtrera TA-fält genom att namnge ett bokmärke som de måste vara inom TOA-gränserna.
    fieldToa.BookmarkName = "MyBookmark";

    // Som standard visas en prickad linje som sträcker sig över hela sidan mellan TA-fältets hänvisningar
    // och dess sidnummer. Vi kan ersätta det med valfri text vi lägger till på den här egenskapen.
    // Om du infogar ett tabbtecken bevaras den ursprungliga tabbteckenet.
    fieldToa.EntrySeparator = " \t p.";

    // Om vi har flera TA-poster som delar samma långa hänvisning,
    // alla deras respektive sidnummer kommer att visas på en rad.
    // Vi kan använda den här egenskapen för att ange en sträng som separerar deras sidnummer.
    fieldToa.PageNumberListSeparator = " & p. ";

    // Vi kan ställa in detta till sant för att få vår tabell att visa ordet "passim"
    // om det finns fem eller fler sidnummer på en rad.
    fieldToa.UsePassim = true;

    // Ett TA-fält kan referera till ett sidintervall.
    // Vi kan ange en sträng här som ska visas mellan start- och slutsidnumren för sådana intervall.
    fieldToa.PageRangeSeparator = " to ";

    // Formatet från TA-fälten kommer att överföras till vår tabell.
    // Vi kan inaktivera detta genom att ställa in flaggan RemoveEntryFormatting.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Detta TA-fält kommer inte att visas som en post i användarvillkoren eftersom det ligger utanför
    // bokmärkets gränser som TOA:s BookmarkName-egenskap anger.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // Detta TA-fält finns inuti bokmärket,
    // men postkategorin matchar inte tabellens, så TA-fältet kommer inte att inkludera den.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // Den här posten kommer att visas i tabellen.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // En TOA-tabell visar inte korta hänvisningar,
    // men vi kan använda dem som en förkortning för att referera till skrymmande källnamn som flera TA-fält refererar till.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // Vi kan formatera sidnumret så att det blir fetstilt/kursivt med hjälp av följande egenskaper.
    // Vi kommer fortfarande att se dessa effekter om vi ställer in vår tabell att ignorera formatering.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // Vi kan konfigurera TA-fält så att deras TOA-poster refererar till ett sidintervall som ett bokmärke sträcker sig över.
    // Observera att den här posten hänvisar till samma källa som den ovan för att dela en rad i vår tabell.
    // Den här raden kommer att innehålla sidnumret för ovanstående post och sidintervallet för denna post,
    // med tabellens sidlista och sidnummerintervallsavgränsare mellan sidnumren.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // Om vi har aktiverat funktionen "Passim" i vår tabell, kommer 5 eller fler TA-poster med samma källa att anropa den.
    for (int i = 0; i < 5; i++)
    {
        InsertToaEntry(builder, "1", "Source 4");
    }

    builder.EndBookmark("MyBookmark");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOA.TA.docx");
}

private static FieldTA InsertToaEntry(DocumentBuilder builder, string entryCategory, string longCitation)
{
    FieldTA field = (FieldTA)builder.InsertField(FieldType.FieldTOAEntry, false);
    field.EntryCategory = entryCategory;
    field.LongCitation = longCitation;

    builder.InsertBreak(BreakType.PageBreak);

    return field;
}
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)

---
title: MailMergeOptions Class
linktitle: MailMergeOptions
articleTitle: MailMergeOptions
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.MailMergeOptions för sömlösa lösningar för dokumentkoppling med låg kod. Förbättra din dokumentautomation med anpassningsbara funktioner!
type: docs
weight: 4260
url: /sv/net/aspose.words.lowcode/mailmergeoptions/
---
## MailMergeOptions class

Representerar alternativ för funktionen för dokumentkoppling.

```csharp
public class MailMergeOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [MailMergeOptions](mailmergeoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CleanupOptions](../../aspose.words.lowcode/mailmergeoptions/cleanupoptions/) { get; set; } | Hämtar eller anger en uppsättning flaggor som anger vilka objekt som ska tas bort under dokumentkoppling. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.lowcode/mailmergeoptions/cleanupparagraphswithpunctuationmarks/) { get; set; } | Hämtar eller anger ett värde som anger om stycken med skiljetecken ska betraktas som tomma och ska tas bort omRemoveEmptyParagraphs alternativet är angivet. |
| [MergeDuplicateRegions](../../aspose.words.lowcode/mailmergeoptions/mergeduplicateregions/) { get; set; } | Hämtar eller anger ett värde som anger om alla dokumentkopplingsområden med namnet på en datakälla ska slås samman vid utskriftskoppling med regioner mot datakällan eller bara den första. |
| [MergeWholeDocument](../../aspose.words.lowcode/mailmergeoptions/mergewholedocument/) { get; set; } | Hämtar eller anger ett värde som anger om fält i hela dokumentet uppdateras när en dokumentkoppling med regioner utförs. |
| [PreserveUnusedTags](../../aspose.words.lowcode/mailmergeoptions/preserveunusedtags/) { get; set; } | Hämtar eller anger ett värde som anger om de oanvända "mustasch"-taggarna ska bevaras. |
| [RegionEndTag](../../aspose.words.lowcode/mailmergeoptions/regionendtag/) { get; set; } | Hämtar eller ställer in en sluttagg för ett regionsavsnitt för dokumentkoppling. |
| [RegionStartTag](../../aspose.words.lowcode/mailmergeoptions/regionstarttag/) { get; set; } | Hämtar eller ställer in en starttagg för en region för dokumentkoppling. |
| [RestartListsAtEachSection](../../aspose.words.lowcode/mailmergeoptions/restartlistsateachsection/) { get; set; } | Hämtar eller anger ett värde som anger om listor startas om i varje avsnitt efter att en dokumentkoppling har utförts. |
| [RetainFirstSectionStart](../../aspose.words.lowcode/mailmergeoptions/retainfirstsectionstart/) { get; set; } | Hämtar eller anger ett värde som anger om sektionsstarten för det första dokumentavsnittet och dess kopior för efterföljande datakällrader behålls under dokumentkoppling eller uppdateras enligt MS Words beteende. |
| [TrimWhitespaces](../../aspose.words.lowcode/mailmergeoptions/trimwhitespaces/) { get; set; } | Hämtar eller anger ett värde som anger om efterföljande och inledande blanksteg ska tas bort från värden för koppling av dokument. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.lowcode/mailmergeoptions/unconditionalmergefieldsandregions/) { get; set; } | Hämtar eller anger ett värde som anger om sammanslagningsfält och sammanslagningsområden slås samman oavsett det överordnade OM-fältets villkor. |
| [UseNonMergeFields](../../aspose.words.lowcode/mailmergeoptions/usenonmergefields/) { get; set; } | När`sann` , anger att utöver MERGEFIELD-fält utförs dokumentkoppling i vissa andra typer av fält och även i "{{fieldName}}"-taggar. |
| [UseWholeParagraphAsRegion](../../aspose.words.lowcode/mailmergeoptions/usewholeparagraphasregion/) { get; set; } | Hämtar eller anger ett värde som anger om hela stycket med**Tabellstart** eller**Bordände** field eller ett visst intervall mellan**Tabellstart** och**Bordände** fält ska inkluderas i området för koppling av dokument. |

## Exempel

Visar hur man utför en dokumentkopplingsoperation för en enskild post.

```csharp
// Det finns flera sätt att göra en dokumentkoppling:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Se även

* namnutrymme [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../)

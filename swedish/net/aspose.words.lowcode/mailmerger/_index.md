---
title: MailMerger Class
linktitle: MailMerger
articleTitle: MailMerger
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.LowCode.MailMerger. Fyll enkelt mallar med data med enkla och avancerade dokumentkopplingstekniker för sömlös dokumentautomation.
type: docs
weight: 4270
url: /sv/net/aspose.words.lowcode/mailmerger/
---
## MailMerger class

Tillhandahåller metoder avsedda att fylla mallen med data med hjälp av enkel dokumentkoppling och dokumentkoppling med regioner.

```csharp
public class MailMerger : Processor
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| static [Create](../../aspose.words.lowcode/mailmerger/create/)(*[MailMergerContext](../mailmergercontext/)*) | Skapar en ny instans av processorn för sammanslagning av e-post. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Utför processoråtgärden. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Anger indatadokument för bearbetning. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Anger indatadokument för bearbetning. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Anger listan över utdatadokumentströmmar. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Anger listan över utdatadokumentströmmar. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Anger utdataströmmen för processorn. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Anger utdataströmmen för processorn. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Anger utdatafilen för processorn. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Anger utdatafilen för processorn. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_12)(*string, string, DataRow*) | Utför koppling av dokument från en DataRow till dokumentet. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_13)(*string, string, DataTable*) | Utför koppling av dokument från en datatabell till dokumentet. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_14)(*string, string, string[], object[]*) | Utför en dokumentkopplingsåtgärd för en enskild post. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Utför en dokumentkopplingsåtgärd för en enskild post. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Utför en dokumentkopplingsåtgärd för en enskild post. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Utför en dokumentkopplingsåtgärd för en enskild post. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_4)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Utför en dokumentkopplingsåtgärd för en enskild post. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_6)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Utför koppling av dokument från en DataRow till dokumentet. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_7)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Utför koppling av dokument från en DataRow till dokumentet. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_9)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Utför koppling av dokument från en DataRow till dokumentet. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_10)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Utför koppling av dokument från en DataRow till dokumentet. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_2)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Utför en dokumentkopplingsåtgärd för en enskild post. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_5)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Utför en dokumentkopplingsåtgärd för en enskild post. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_8)(*string, string, [SaveFormat](../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Utför en dokumentkopplingsåtgärd för en enskild post. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_11)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Utför en dokumentkopplingsåtgärd för en enskild post. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Utför dokumentkoppling från en DataRow till dokumentet och renderar resultatet som bilder. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_1)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Utför dokumentkoppling från en DataRow till dokumentet och renderar resultatet som bilder. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_3)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Utför dokumentkoppling från en DataRow till dokumentet och renderar resultatet som bilder. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_4)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Utför dokumentkoppling från en DataRow till dokumentet och renderar resultatet som bilder. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_2)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Utför en dokumentkopplingsoperation för en enskild post och renderar resultatet som bilder. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_5)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Utför en dokumentkopplingsoperation för en enskild post och renderar resultatet som bilder. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_8)(*string, string, DataSet*) | Utför koppling av dokument från en datauppsättning till ett dokument med kopplingsområden. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_9)(*string, string, DataTable*) | Utför dokumentkoppling från en datatabell till dokumentet med områden för dokumentkoppling. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Utför koppling av dokument från en datauppsättning till dokumentet med kopplingsområden. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Utför en dokumentkopplingsåtgärd för en enskild post. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_2)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Utför koppling av dokument från en datauppsättning till dokumentet med kopplingsområden. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Utför en dokumentkopplingsåtgärd för en enskild post. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_4)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Utför koppling av dokument från en datauppsättning till dokumentet med kopplingsområden. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_5)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Utför dokumentkoppling från en datatabell till dokumentet med områden för dokumentkoppling. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_6)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Utför koppling av dokument från en datauppsättning till dokumentet med kopplingsområden. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_7)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Utför dokumentkoppling från en datatabell till dokumentet med områden för dokumentkoppling. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Utför koppling av dokument från en datauppsättning till dokumentet med kopplingsområden och renderar resultatet som bilder. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages_1)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Utför dokumentkoppling från en datatabell till dokumentet med områden för dokumentkoppling och renderar resultatet som bilder. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages_2)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Utför koppling av dokument från en datauppsättning till dokumentet med kopplingsområden och renderar resultatet som bilder. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages_3)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Utför dokumentkoppling från en datatabell till dokumentet med områden för dokumentkoppling och renderar resultatet som bilder. |

### Se även

* class [Processor](../processor/)
* namnutrymme [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../)

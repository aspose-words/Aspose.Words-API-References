---
title: ReportBuilder Class
linktitle: ReportBuilder
articleTitle: ReportBuilder
second_title: Aspose.Words för .NET
description: Skapa enkelt dynamiska rapporter med Aspose.Words LowCode ReportBuilder. Använd LINQ Reporting Engine för att fylla mallar med data sömlöst.
type: docs
weight: 4360
url: /sv/net/aspose.words.lowcode/reportbuilder/
---
## ReportBuilder class

Tillhandahåller metoder avsedda att fylla mallen med data med hjälp av LINQ Reporting Engine.

```csharp
public class ReportBuilder : Processor
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| static [Create](../../aspose.words.lowcode/reportbuilder/create/#create)() | Skapar en ny instans av rapportbyggarens processor. |
| static [Create](../../aspose.words.lowcode/reportbuilder/create/#create_1)(*[ReportBuilderContext](../reportbuildercontext/)*) | Skapar en ny instans av rapportbyggarens processor. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Utför processoråtgärden. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Anger indatadokument för bearbetning. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Anger indatadokument för bearbetning. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Anger listan över utdatadokumentströmmar. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Anger listan över utdatadokumentströmmar. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Anger utdataströmmen för processorn. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Anger utdataströmmen för processorn. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Anger utdatafilen för processorn. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Anger utdatafilen för processorn. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_12)(*string, string, object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Fyller malldokumentet med data från den angivna källan och genererar en färdig rapport med ytterligare alternativ. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Fyller malldokumentet med data från den angivna källan och genererar en färdig rapport med angivet utdataformat och ytterligare alternativ, från in- och utdataströmmar. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Fyller malldokumentet med data från den angivna källan och genererar en färdig rapport med angivet utdataformat och ytterligare alternativ, från in- och utdataströmmar. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_13)(*string, string, object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Fyller malldokumentet med data från den angivna källan och genererar en färdig rapport med en namngiven datakällreferens och ytterligare alternativ. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_14)(*string, string, object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Fyller malldokumentet med data från flera källor och genererar en färdig rapport med ytterligare alternativ. Denna överbelastning avgör automatiskt sparformatet baserat på utdatafiländelsen. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_6)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Fyller malldokumentet med data från den angivna källan och genererar en färdig rapport med angivet utdataformat och ytterligare alternativ. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_9)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Fyller malldokumentet med data från den angivna källan och genererar en färdig rapport med angivet utdataformat och ytterligare alternativ. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Fyller malldokumentet med data från den angivna källan och genererar en färdig rapport med en namngiven datakällreferens och ytterligare alternativ. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_2)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Fyller malldokumentet med data från flera källor och genererar en färdig rapport med angivet utdataformat och ytterligare alternativ från de angivna in- och utdatafilströmmarna. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_4)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Fyller malldokumentet med data från den angivna källan och genererar en färdig rapport med en namngiven datakällreferens och ytterligare alternativ. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_5)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Fyller malldokumentet med data från flera källor och genererar en färdig rapport med angivet utdataformat och ytterligare alternativ från de angivna in- och utdatafilströmmarna. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_7)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Fyller malldokumentet med data från den angivna källan och genererar en färdig rapport med angivet utdataformat, en namngiven datakällreferens och ytterligare alternativ. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_8)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Fyller malldokumentet med data från flera källor och genererar en färdig rapport med ett angivet utdataformat och ytterligare alternativ. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_10)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Fyller malldokumentet med data från den angivna källan och genererar en färdig rapport med angivet utdataformat, en namngiven datakällreferens och ytterligare alternativ. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_11)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Fyller malldokumentet med data från flera källor och genererar en färdig rapport med ett angivet utdataformat och ytterligare alternativ. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Fyller malldokumentet med data från flera källor. Återger utdata till bilder. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages_1)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Fyller malldokumentet med data från flera källor. Återger utdata till bilder. |

### Se även

* class [Processor](../processor/)
* namnutrymme [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../)

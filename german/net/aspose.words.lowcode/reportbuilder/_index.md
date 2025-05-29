---
title: ReportBuilder Class
linktitle: ReportBuilder
articleTitle: ReportBuilder
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos dynamische Berichte mit Aspose.Words LowCode ReportBuilder. Nutzen Sie die LINQ Reporting Engine, um Vorlagen nahtlos mit Daten zu füllen.
type: docs
weight: 4360
url: /de/net/aspose.words.lowcode/reportbuilder/
---
## ReportBuilder class

Bietet Methoden zum Füllen von Vorlagen mit Daten mithilfe der LINQ Reporting Engine.

```csharp
public class ReportBuilder : Processor
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| static [Create](../../aspose.words.lowcode/reportbuilder/create/#create)() | Erstellt eine neue Instanz des Report Builder-Prozessors. |
| static [Create](../../aspose.words.lowcode/reportbuilder/create/#create_1)(*[ReportBuilderContext](../reportbuildercontext/)*) | Erstellt eine neue Instanz des Report Builder-Prozessors. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Führen Sie die Prozessoraktion aus. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Gibt das Eingabedokument für die Verarbeitung an. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Gibt die Liste der Ausgabedokumentströme an. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Gibt die Liste der Ausgabedokumentströme an. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Gibt den Ausgabestream für den Prozessor an. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Gibt den Ausgabestream für den Prozessor an. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Gibt die Ausgabedatei für den Prozessor an. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_12)(*string, string, object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert einen vollständigen Bericht mit zusätzlichen Optionen. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert aus Eingabe- und Ausgabeströmen einen vollständigen Bericht mit dem angegebenen Ausgabeformat und zusätzlichen Optionen. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert aus Eingabe- und Ausgabeströmen einen vollständigen Bericht mit dem angegebenen Ausgabeformat und zusätzlichen Optionen. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_13)(*string, string, object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert einen vollständigen Bericht mit einer benannten Datenquellenreferenz und zusätzlichen Optionen. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_14)(*string, string, object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Füllt das Vorlagendokument mit Daten aus mehreren Quellen und generiert einen vollständigen Bericht mit zusätzlichen Optionen. Diese Überladung bestimmt automatisch das Speicherformat basierend auf der Ausgabedateierweiterung. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_6)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert einen vollständigen Bericht mit dem angegebenen Ausgabeformat und zusätzlichen Optionen. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_9)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert einen vollständigen Bericht mit dem angegebenen Ausgabeformat und zusätzlichen Optionen. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert einen vollständigen Bericht mit einer benannten Datenquellenreferenz und zusätzlichen Optionen. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_2)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Füllt das Vorlagendokument mit Daten aus mehreren Quellen und generiert einen vollständigen Bericht mit dem angegebenen Ausgabeformat und zusätzlichen Optionen aus den angegebenen Eingabe- und Ausgabedateiströmen. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_4)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert einen vollständigen Bericht mit einer benannten Datenquellenreferenz und zusätzlichen Optionen. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_5)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Füllt das Vorlagendokument mit Daten aus mehreren Quellen und generiert einen vollständigen Bericht mit dem angegebenen Ausgabeformat und zusätzlichen Optionen aus den angegebenen Eingabe- und Ausgabedateiströmen. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_7)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert einen vollständigen Bericht mit dem angegebenen Ausgabeformat, einer benannten Datenquellenreferenz und zusätzlichen Optionen. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_8)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Füllt das Vorlagendokument mit Daten aus mehreren Quellen und generiert einen vollständigen Bericht mit einem angegebenen Ausgabeformat und zusätzlichen Optionen. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_10)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Füllt das Vorlagendokument mit Daten aus der angegebenen Quelle und generiert einen vollständigen Bericht mit dem angegebenen Ausgabeformat, einer benannten Datenquellenreferenz und zusätzlichen Optionen. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_11)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Füllt das Vorlagendokument mit Daten aus mehreren Quellen und generiert einen vollständigen Bericht mit einem angegebenen Ausgabeformat und zusätzlichen Optionen. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Füllt das Vorlagendokument mit Daten aus mehreren Quellen. Rendert die Ausgabe in Bilder. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages_1)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Füllt das Vorlagendokument mit Daten aus mehreren Quellen. Rendert die Ausgabe in Bilder. |

### Siehe auch

* class [Processor](../processor/)
* namensraum [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../)

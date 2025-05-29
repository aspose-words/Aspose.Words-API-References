---
title: Converter Class
linktitle: Converter
articleTitle: Converter
second_title: Aspose.Words für .NET
description: Konvertieren Sie mühelos verschiedene Dokumenttypen mit Aspose.Words.LowCode.Converter. Vereinfachen Sie Ihren Workflow mit nur einer Codezeile für eine nahtlose Integration.
type: docs
weight: 4230
url: /de/net/aspose.words.lowcode/converter/
---
## Converter class

Stellt eine Gruppe von Methoden dar, die dazu dienen, eine Vielzahl unterschiedlicher Dokumenttypen mit einer einzigen Codezeile zu konvertieren.

```csharp
public class Converter : Processor
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| static [Create](../../aspose.words.lowcode/converter/create/#create)() | Erstellt eine neue Instanz des Konverterprozessors. |
| static [Create](../../aspose.words.lowcode/converter/create/#create_1)(*[ConverterContext](../convertercontext/)*) | Erstellt eine neue Instanz des Konverterprozessors. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Führen Sie die Prozessoraktion aus. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Gibt das Eingabedokument für die Verarbeitung an. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Gibt die Liste der Ausgabedokumentströme an. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Gibt die Liste der Ausgabedokumentströme an. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Gibt den Ausgabestream für den Prozessor an. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Gibt den Ausgabestream für den Prozessor an. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Gibt die Ausgabedatei für den Prozessor an. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_4)(*string, string*) | Konvertiert das angegebene Eingabedokument unter Verwendung der angegebenen Eingabe-/Ausgabedateinamen und -erweiterungen in das Ausgabedokument. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Konvertiert das angegebene Eingabedokument unter Verwendung der angegebenen Eingabe- und Ausgabeströme in ein einzelnes Ausgabedokument. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_2)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Konvertiert das angegebene Eingabedokument unter Verwendung der angegebenen Eingabe- und Ausgabeströme in ein einzelnes Ausgabedokument. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_5)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Konvertiert das angegebene Eingabedokument unter Verwendung der angegebenen Eingabe-/Ausgabedateinamen und des endgültigen Dokumentformats in das Ausgabedokument. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_6)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Konvertiert das angegebene Eingabedokument unter Verwendung der angegebenen Eingabe-/Ausgabedateinamen und Speicheroptionen in das Ausgabedokument. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Konvertiert das angegebene Eingabedokument unter Verwendung der angegebenen Eingabe- und Ausgabeströme in ein einzelnes Ausgabedokument. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/), string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Konvertiert das angegebene Eingabedokument unter Verwendung der angegebenen Eingabe-/Ausgabedateinamen und seiner Lade-/Speicheroptionen in das Ausgabedokument. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_1)(*[Document](../../aspose.words/document/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Konvertiert die Seiten des angegebenen Dokuments unter Verwendung der angegebenen Speicheroptionen in Bilder und gibt ein Array von Streams zurück, die die Bilder enthalten. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages)(*[Document](../../aspose.words/document/), [SaveFormat](../../aspose.words/saveformat/)*) | Konvertiert die Seiten des angegebenen Dokuments in Bilder im angegebenen Format und gibt ein Array von Streams zurück, die die Bilder enthalten. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_4)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Konvertiert die Seiten des angegebenen Eingabestreams unter Verwendung der angegebenen Speicheroptionen in Bilder und gibt ein Array von Streams zurück, die die Bilder enthalten. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_3)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Konvertiert die Seiten des angegebenen Eingabestreams in Bilder im angegebenen Format und gibt ein Array von Streams zurück, die die Bilder enthalten. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_6)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Konvertiert die Seiten der angegebenen Eingabedatei unter Verwendung der angegebenen Speicheroptionen in Bilder und gibt ein Array von Streams zurück, die die Bilder enthalten. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_5)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Konvertiert die Seiten der angegebenen Eingabedatei in Bilder im angegebenen Format und gibt ein Array von Streams zurück, die die Bilder enthalten. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Konvertiert die Seiten des angegebenen Eingabestreams mithilfe der bereitgestellten Lade- und Speicheroptionen in Bilder und gibt ein Array von Streams zurück, die die Bilder enthalten. |

## Bemerkungen

Die angegebenen Eingabe- und Ausgabedateien bzw. -streams sowie das gewünschte Speicherformat werden verwendet, um das angegebene Eingabedokument des einen Formats in das Ausgabedokument des anderen angegebenen Formats zu konvertieren.

Die Konvertierungsfunktion unterstützt über 35 verschiedene Dateiformate.

Der[`ConvertToImages`](./converttoimages/)Eine Gruppe von Methoden dient der Umwandlung von Dokumenten in Bilder, wobei jede Seite in eine separate Bilddatei konvertiert wird. Diese Methoden konvertieren PDF-Dokumente auch direkt in Festseitenformate, ohne sie in das Dokumentmodell zu laden. Dies verbessert sowohl die Leistung als auch die Genauigkeit.

Mit[`PageSet`](../../aspose.words.saving/imagesaveoptions/pageset/)können Sie einen bestimmten Satz von Seiten angeben, die in Bilder konvertiert werden sollen.

### Siehe auch

* class [Processor](../processor/)
* namensraum [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../)

---
title: Splitter Class
linktitle: Splitter
articleTitle: Splitter
second_title: Aspose.Words für .NET
description: Teilen Sie Dokumente mühelos mit der Klasse Aspose.Words.LowCode.Splitter. Nutzen Sie vielseitige Methoden für präzises Dokumentenmanagement und verbesserte Workflow-Effizienz.
type: docs
weight: 4420
url: /de/net/aspose.words.lowcode/splitter/
---
## Splitter class

Bietet Methoden zum Aufteilen der Dokumente nach unterschiedlichen Kriterien.

```csharp
public class Splitter : Processor
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| static [Create](../../aspose.words.lowcode/splitter/create/)(*[SplitterContext](../splittercontext/)*) | Erstellt eine neue Instanz des Splitterprozessors. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Führen Sie die Prozessoraktion aus. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Gibt das Eingabedokument für die Verarbeitung an. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Gibt die Liste der Ausgabedokumentströme an. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Gibt die Liste der Ausgabedokumentströme an. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Gibt den Ausgabestream für den Prozessor an. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Gibt den Ausgabestream für den Prozessor an. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Gibt die Ausgabedatei für den Prozessor an. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_4)(*string, string, int, int*) | Extrahiert einen angegebenen Seitenbereich aus einer Dokumentdatei und speichert die extrahierten Seiten in einer neuen Datei. Das Ausgabedateiformat wird durch die Erweiterung des Ausgabedateinamens bestimmt. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), int, int*) | Extrahiert einen angegebenen Seitenbereich aus einem Dokumentstream und speichert die extrahierten Seiten unter Verwendung des angegebenen Speicherformats in einem Ausgabestream. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | Extrahiert einen angegebenen Seitenbereich aus einem Dokumentstream und speichert die extrahierten Seiten unter Verwendung des angegebenen Speicherformats in einem Ausgabestream. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_2)(*string, string, [SaveFormat](../../aspose.words/saveformat/), int, int*) | Extrahiert einen angegebenen Seitenbereich aus einer Dokumentdatei und speichert die extrahierten Seiten im angegebenen Speicherformat in einer neuen Datei. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_3)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | Extrahiert einen angegebenen Seitenbereich aus einer Dokumentdatei und speichert die extrahierten Seiten im angegebenen Speicherformat in einer neuen Datei. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_2)(*string, string*) | Entfernt leere Seiten aus dem Dokument und speichert die Ausgabe. Gibt eine Liste der entfernten Seitenzahlen zurück. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Entfernt leere Seiten aus einem Dokument, das in einem Eingabestream bereitgestellt wird, und speichert das aktualisierte Dokument im angegebenen Speicherformat in einem Ausgabestream. Gibt eine Liste der entfernten Seitenzahlen zurück. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Entfernt leere Seiten aus einem Dokument, das in einem Eingabestream bereitgestellt wird, und speichert das aktualisierte Dokument im angegebenen Speicherformat in einem Ausgabestream. Gibt eine Liste der entfernten Seitenzahlen zurück. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Entfernt leere Seiten aus dem Dokument und speichert die Ausgabe im angegebenen Format. Gibt eine Liste der entfernten Seitenzahlen zurück. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Entfernt leere Seiten aus dem Dokument und speichert die Ausgabe im angegebenen Format. Gibt eine Liste der entfernten Seitenzahlen zurück. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split)(*Stream, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | Teilt ein Dokument aus einem Eingabestream basierend auf den angegebenen Teilungsoptionen in mehrere Teile auf und gibt die resultierenden Teile als Array von Streams im angegebenen Speicherformat zurück. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | Teilt ein Dokument aus einem Eingabestream basierend auf den angegebenen Teilungsoptionen in mehrere Teile auf und gibt die resultierenden Teile als Array von Streams im angegebenen Speicherformat zurück. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_2)(*string, string, [SplitOptions](../splitoptions/)*) | Teilt ein Dokument basierend auf den angegebenen Teiloptionen in mehrere Teile auf und speichert die resultierenden Teile in Dateien. Das Ausgabedateiformat wird durch die Erweiterung des Ausgabedateinamens bestimmt. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | Teilt ein Dokument basierend auf den angegebenen Teiloptionen in mehrere Teile auf und speichert die resultierenden Teile in Dateien im angegebenen Speicherformat. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | Teilt ein Dokument basierend auf den angegebenen Teiloptionen in mehrere Teile auf und speichert die resultierenden Teile in Dateien im angegebenen Speicherformat. |

### Siehe auch

* class [Processor](../processor/)
* namensraum [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../)

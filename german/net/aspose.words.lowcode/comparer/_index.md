---
title: Comparer Class
linktitle: Comparer
articleTitle: Comparer
second_title: Aspose.Words für .NET
description: Vergleichen Sie Dokumente mühelos mit der Aspose.Words LowCode Comparer-Klasse. Nutzen Sie leistungsstarke Methoden für nahtlose Dokumentenanalyse und Zusammenarbeit.
type: docs
weight: 4210
url: /de/net/aspose.words.lowcode/comparer/
---
## Comparer class

Stellt Methoden zum Vergleichen von Dokumenten bereit.

```csharp
public class Comparer : Processor
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| static [Create](../../aspose.words.lowcode/comparer/create/#create)() | Erstellt eine neue Instanz des Konverterprozessors. |
| static [Create](../../aspose.words.lowcode/comparer/create/#create_1)(*[ComparerContext](../comparercontext/)*) | Erstellt eine neue Instanz des Vergleichsprozessors. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Führen Sie die Prozessoraktion aus. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Gibt das Eingabedokument für die Verarbeitung an. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Gibt das Eingabedokument für die Verarbeitung an. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Gibt die Liste der Ausgabedokumentströme an. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Gibt die Liste der Ausgabedokumentströme an. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Gibt den Ausgabestream für den Prozessor an. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Gibt den Ausgabestream für den Prozessor an. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Gibt die Ausgabedatei für den Prozessor an. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Gibt die Ausgabedatei für den Prozessor an. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_4)(*string, string, string, string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in der angegebenen Ausgabedatei. Dabei werden Änderungen als eine Reihe von Bearbeitungs- und Formatrevisionen erstellt. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare)(*Stream, Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Vergleicht zwei aus Streams geladene Dokumente mit zusätzlichen Optionen und speichert die Unterschiede im angegebenen Ausgabestream im angegebenen Speicherformat. Dabei werden Änderungen als eine Reihe von Bearbeitungs- und Formatrevisionen erzeugt. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_1)(*Stream, Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Vergleicht zwei aus Streams geladene Dokumente mit zusätzlichen Optionen und speichert die Unterschiede im angegebenen Ausgabestream im angegebenen Speicherformat. Dabei werden Änderungen als eine Reihe von Bearbeitungs- und Formatrevisionen erzeugt. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_2)(*string, string, string, [SaveFormat](../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in der angegebenen Ausgabedatei im bereitgestellten Speicherformat. Dabei werden Änderungen als eine Reihe von Bearbeitungs- und Formatrevisionen erstellt. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_3)(*string, string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in der angegebenen Ausgabedatei im bereitgestellten Speicherformat. Dabei werden Änderungen als eine Reihe von Bearbeitungs- und Formatrevisionen erstellt. |
| static [CompareToImages](../../aspose.words.lowcode/comparer/comparetoimages/#comparetoimages)(*Stream, Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. Jedes Element im zurückgegebenen Array stellt eine einzelne Seite der als Bild gerenderten Ausgabe dar. |
| static [CompareToImages](../../aspose.words.lowcode/comparer/comparetoimages/#comparetoimages_1)(*string, string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. Jedes Element im zurückgegebenen Array stellt eine einzelne Seite der als Bild gerenderten Ausgabe dar. |

### Siehe auch

* class [Processor](../processor/)
* namensraum [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../)

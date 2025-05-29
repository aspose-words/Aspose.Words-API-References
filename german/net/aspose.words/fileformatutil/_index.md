---
title: FileFormatUtil Class
linktitle: FileFormatUtil
articleTitle: FileFormatUtil
second_title: Aspose.Words für .NET
description: Verwalten Sie Dateiformate mühelos mit Aspose.Words.FileFormatUtil. Erkennen Sie Formate und konvertieren Sie Erweiterungen nahtlos für mehr Produktivität.
type: docs
weight: 3230
url: /de/net/aspose.words/fileformatutil/
---
## FileFormatUtil class

Bietet Dienstprogrammmethoden für die Arbeit mit Dateiformaten, z. B. zum Erkennen von Dateiformaten oder zum Konvertieren von Dateierweiterungen in/aus Dateiformat-Enumerationen.

Um mehr zu erfahren, besuchen Sie die[Dateiformat erkennen und Formatkompatibilität prüfen](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) Dokumentationsartikel.

```csharp
public static class FileFormatUtil
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| static [ContentTypeToLoadFormat](../../aspose.words/fileformatutil/contenttypetoloadformat/)(*string*) | Konvertiert den IANA-Inhaltstyp in einen Aufzählungswert im Ladeformat. |
| static [ContentTypeToSaveFormat](../../aspose.words/fileformatutil/contenttypetosaveformat/)(*string*) | Konvertiert den IANA-Inhaltstyp in einen aufgezählten Wert im sicheren Format. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat)(*Stream*) | Erkennt und gibt die Informationen zum Format eines in einem Stream gespeicherten Dokuments zurück. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat_1)(*string*) | Erkennt und gibt die Informationen zum Format eines in einer Datei gespeicherten Dokuments zurück. |
| static [ExtensionToSaveFormat](../../aspose.words/fileformatutil/extensiontosaveformat/)(*string*) | Wandelt eine Dateinamenerweiterung in eine[`SaveFormat`](../saveformat/) Wert. |
| static [ImageTypeToExtension](../../aspose.words/fileformatutil/imagetypetoextension/)(*[ImageType](../../aspose.words.drawing/imagetype/)*) | Konvertiert einen Aufzählungswert des Bildtyps Aspose.Words in eine Dateierweiterung. Die zurückgegebene Erweiterung ist eine Zeichenfolge in Kleinbuchstaben mit einem führenden Punkt. |
| static [LoadFormatToExtension](../../aspose.words/fileformatutil/loadformattoextension/)(*[LoadFormat](../loadformat/)*) | Konvertiert einen im Ladeformat aufgezählten Wert in eine Dateierweiterung. Die zurückgegebene Erweiterung ist eine Zeichenfolge in Kleinbuchstaben mit einem führenden Punkt. |
| static [LoadFormatToSaveFormat](../../aspose.words/fileformatutil/loadformattosaveformat/)(*[LoadFormat](../loadformat/)*) | Konvertiert eine[`LoadFormat`](../loadformat/) Wert zu einem[`SaveFormat`](../saveformat/) Wert wenn möglich. |
| static [SaveFormatToExtension](../../aspose.words/fileformatutil/saveformattoextension/)(*[SaveFormat](../saveformat/)*) | Konvertiert einen Enumerationswert im Speicherformat in eine Dateierweiterung. Die zurückgegebene Erweiterung ist eine Zeichenfolge in Kleinbuchstaben mit einem führenden Punkt. |
| static [SaveFormatToLoadFormat](../../aspose.words/fileformatutil/saveformattoloadformat/)(*[SaveFormat](../saveformat/)*) | Konvertiert eine[`SaveFormat`](../saveformat/) Wert zu einem[`LoadFormat`](../loadformat/) Wert wenn möglich. |

## Beispiele

Zeigt, wie die Kodierung in einer HTML-Datei erkannt wird.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// Die Encoding-Eigenschaft wird nur verwendet, wenn wir ein FileFormatInfo-Objekt für ein HTML-Dokument erstellen.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)

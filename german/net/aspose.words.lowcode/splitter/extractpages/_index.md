---
title: Splitter.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words für .NET
description: Extrahieren Sie mühelos bestimmte Seiten aus jedem Dokument mit unserer Splitter-ExtractPages-Methode. Speichern Sie sie im gewünschten Format für einfachen Zugriff!
type: docs
weight: 20
url: /de/net/aspose.words.lowcode/splitter/extractpages/
---
## ExtractPages(*string, string, int, int*) {#extractpages_4}

Extrahiert einen angegebenen Seitenbereich aus einer Dokumentdatei und speichert die extrahierten Seiten in einer neuen Datei. Das Ausgabedateiformat wird durch die Erweiterung des Ausgabedateinamens bestimmt.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, int startPageIndex, 
    int pageCount)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| startPageIndex | Int32 | Der nullbasierte Index der ersten zu extrahierenden Seite. |
| pageCount | Int32 | Anzahl der zu extrahierenden Seiten. |

## Beispiele

Zeigt, wie Seiten aus dem Dokument extrahiert werden.

```csharp
// Es gibt mehrere Möglichkeiten, Seiten aus dem Dokument zu extrahieren:
string doc = MyDir + "Big document.docx";

Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.1.docx", 0, 2);
Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.2.docx", SaveFormat.Docx, 0, 2);
```

### Siehe auch

* class [Splitter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExtractPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/), int, int*) {#extractpages_2}

Extrahiert einen angegebenen Seitenbereich aus einer Dokumentdatei und speichert die extrahierten Seiten im angegebenen Speicherformat in einer neuen Datei.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    int startPageIndex, int pageCount)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveFormat | SaveFormat | Das Speicherformat. |
| startPageIndex | Int32 | Der nullbasierte Index der ersten zu extrahierenden Seite. |
| pageCount | Int32 | Anzahl der zu extrahierenden Seiten. |

## Beispiele

Zeigt, wie Seiten aus dem Dokument extrahiert werden.

```csharp
// Es gibt mehrere Möglichkeiten, Seiten aus dem Dokument zu extrahieren:
string doc = MyDir + "Big document.docx";

Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.1.docx", 0, 2);
Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.2.docx", SaveFormat.Docx, 0, 2);
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExtractPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), int, int*) {#extractpages_3}

Extrahiert einen angegebenen Seitenbereich aus einer Dokumentdatei und speichert die extrahierten Seiten im angegebenen Speicherformat in einer neuen Datei.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, int startPageIndex, int pageCount)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveOptions | SaveOptions | Die Speicheroptionen. |
| startPageIndex | Int32 | Der nullbasierte Index der ersten zu extrahierenden Seite. |
| pageCount | Int32 | Anzahl der zu extrahierenden Seiten. |

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExtractPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), int, int*) {#extractpages}

Extrahiert einen angegebenen Seitenbereich aus einem Dokumentstream und speichert die extrahierten Seiten unter Verwendung des angegebenen Speicherformats in einem Ausgabestream.

```csharp
public static void ExtractPages(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    int startPageIndex, int pageCount)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabestream. |
| outputStream | Stream | Der Ausgabestream. |
| saveFormat | SaveFormat | Das Speicherformat. |
| startPageIndex | Int32 | Der nullbasierte Index der ersten zu extrahierenden Seite. |
| pageCount | Int32 | Anzahl der zu extrahierenden Seiten. |

## Beispiele

Zeigt, wie Seiten aus dem Dokument aus dem Stream extrahiert werden.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ExtractPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.ExtractPages(streamIn, streamOut, SaveFormat.Docx, 0, 2);
}
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExtractPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), int, int*) {#extractpages_1}

Extrahiert einen angegebenen Seitenbereich aus einem Dokumentstream und speichert die extrahierten Seiten unter Verwendung des angegebenen Speicherformats in einem Ausgabestream.

```csharp
public static void ExtractPages(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    int startPageIndex, int pageCount)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabestream. |
| outputStream | Stream | Der Ausgabestream. |
| saveOptions | SaveOptions | Die Speicheroptionen. |
| startPageIndex | Int32 | Der nullbasierte Index der ersten zu extrahierenden Seite. |
| pageCount | Int32 | Anzahl der zu extrahierenden Seiten. |

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

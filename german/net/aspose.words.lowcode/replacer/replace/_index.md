---
title: Replacer.Replace
linktitle: Replace
articleTitle: Replace
second_title: Aspose.Words für .NET
description: Ersetzen Sie mühelos alle Vorkommen einer bestimmten Zeichenfolge in Ihrer Eingabedatei mit der Replacer-Methode. Optimieren Sie Ihre Textbearbeitung noch heute!
type: docs
weight: 20
url: /de/net/aspose.words.lowcode/replacer/replace/
---
## Replace(*string, string, string, string*) {#replace_8}

Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge in der Eingabedatei.

```csharp
public static int Replace(string inputFileName, string outputFileName, string pattern, 
    string replacement)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| pattern | String | Eine zu ersetzende Zeichenfolge. |
| replacement | String | Eine Zeichenfolge zum Ersetzen aller Vorkommen des Musters. |

### Rückgabewert

Die Anzahl der vorgenommenen Ersetzungen.

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie Zeichenfolgen im Dokument ersetzt werden.

```csharp
// Es gibt mehrere Möglichkeiten, Zeichenfolgen im Dokument zu ersetzen:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.3.docx", SaveFormat.Docx, pattern, replacement, options);
```

### Siehe auch

* class [Replacer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_4}

Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge in der Eingabedatei, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveFormat | SaveFormat | Das Speicherformat. |
| pattern | String | Eine zu ersetzende Zeichenfolge. |
| replacement | String | Eine Zeichenfolge zum Ersetzen aller Vorkommen des Musters. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) Objekt, um zusätzliche Optionen anzugeben. |

### Rückgabewert

Die Anzahl der vorgenommenen Ersetzungen.

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie Zeichenfolgen im Dokument ersetzt werden.

```csharp
// Es gibt mehrere Möglichkeiten, Zeichenfolgen im Dokument zu ersetzen:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.3.docx", SaveFormat.Docx, pattern, replacement, options);
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_6}

Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge in der Eingabedatei, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveOptions | SaveOptions | Die Speicheroptionen. |
| pattern | String | Eine zu ersetzende Zeichenfolge. |
| replacement | String | Eine Zeichenfolge zum Ersetzen aller Vorkommen des Musters. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) Objekt, um zusätzliche Optionen anzugeben. |

### Rückgabewert

Die Anzahl der vorgenommenen Ersetzungen.

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace}

Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge im Eingabestream, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabestream. |
| outputStream | Stream | Der Ausgabestream. |
| saveFormat | SaveFormat | Das Speicherformat. |
| pattern | String | Eine zu ersetzende Zeichenfolge. |
| replacement | String | Eine Zeichenfolge zum Ersetzen aller Vorkommen des Musters. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) Objekt, um zusätzliche Optionen anzugeben. |

### Rückgabewert

Die Anzahl der vorgenommenen Ersetzungen.

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

## Beispiele

Zeigt, wie Zeichenfolgen im Dokument durch Dokumente aus dem Stream ersetzt werden.

```csharp
// Es gibt mehrere Möglichkeiten, Zeichenfolgen im Dokument durch Dokumente aus dem Stream zu ersetzen:
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
    {
        FindReplaceOptions options = new FindReplaceOptions();
        options.FindWholeWordsOnly = false;
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement, options);
    }
}
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_2}

Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge im Eingabestream, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabestream. |
| outputStream | Stream | Der Ausgabestream. |
| saveOptions | SaveOptions | Die Speicheroptionen. |
| pattern | String | Eine zu ersetzende Zeichenfolge. |
| replacement | String | Eine Zeichenfolge zum Ersetzen aller Vorkommen des Musters. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) Objekt, um zusätzliche Optionen anzugeben. |

### Rückgabewert

Die Anzahl der vorgenommenen Ersetzungen.

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Replace(*string, string, Regex, string*) {#replace_9}

Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters mithilfe eines regulären Ausdrucks durch eine Ersatzzeichenfolge in der Eingabedatei.

```csharp
public static int Replace(string inputFileName, string outputFileName, Regex pattern, 
    string replacement)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| pattern | Regex | Ein reguläres Ausdrucksmuster zum Suchen von Übereinstimmungen. |
| replacement | String | Eine Zeichenfolge zum Ersetzen aller Vorkommen des Musters. |

### Rückgabewert

Die Anzahl der vorgenommenen Ersetzungen.

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie Zeichenfolgen im Dokument durch reguläre Ausdrücke ersetzt werden.

```csharp
// Es gibt mehrere Möglichkeiten, Zeichenfolgen im Dokument durch reguläre Ausdrücke zu ersetzen:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.3.docx", SaveFormat.Docx, pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### Siehe auch

* class [Replacer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveFormat](../../../aspose.words/saveformat/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_5}

Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge in der Eingabedatei unter Verwendung eines regulären Ausdrucks, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveFormat | SaveFormat | Das Speicherformat. |
| pattern | Regex | Ein reguläres Ausdrucksmuster zum Suchen von Übereinstimmungen. |
| replacement | String | Eine Zeichenfolge zum Ersetzen aller Vorkommen des Musters. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) Objekt, um zusätzliche Optionen anzugeben. |

### Rückgabewert

Die Anzahl der vorgenommenen Ersetzungen.

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie Zeichenfolgen im Dokument durch reguläre Ausdrücke ersetzt werden.

```csharp
// Es gibt mehrere Möglichkeiten, Zeichenfolgen im Dokument durch reguläre Ausdrücke zu ersetzen:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.3.docx", SaveFormat.Docx, pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_7}

Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge in der Eingabedatei unter Verwendung eines regulären Ausdrucks, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveOptions | SaveOptions | Die Speicheroptionen. |
| pattern | Regex | Ein reguläres Ausdrucksmuster zum Suchen von Übereinstimmungen. |
| replacement | String | Eine Zeichenfolge zum Ersetzen aller Vorkommen des Musters. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) Objekt, um zusätzliche Optionen anzugeben. |

### Rückgabewert

Die Anzahl der vorgenommenen Ersetzungen.

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_1}

Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge im Eingabestrom unter Verwendung eines regulären Ausdrucks, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabestream. |
| outputStream | Stream | Der Ausgabestream. |
| saveFormat | SaveFormat | Das Speicherformat. |
| pattern | Regex | Ein reguläres Ausdrucksmuster zum Suchen von Übereinstimmungen. |
| replacement | String | Eine Zeichenfolge zum Ersetzen aller Vorkommen des Musters. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) Objekt, um zusätzliche Optionen anzugeben. |

### Rückgabewert

Die Anzahl der vorgenommenen Ersetzungen.

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

## Beispiele

Zeigt, wie Zeichenfolgen im Dokument mithilfe von Dokumenten aus dem Stream durch reguläre Ausdrücke ersetzt werden.

```csharp
// Es gibt mehrere Möglichkeiten, Zeichenfolgen im Dokument mithilfe von Dokumenten aus dem Stream durch reguläre Ausdrücke zu ersetzen:
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStreamRegex.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStreamRegex.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
}
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_3}

Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge im Eingabestrom unter Verwendung eines regulären Ausdrucks, mit dem angegebenen Speicherformat und zusätzlichen Optionen.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabestream. |
| outputStream | Stream | Der Ausgabestream. |
| saveOptions | SaveOptions | Die Speicheroptionen. |
| pattern | Regex | Ein reguläres Ausdrucksmuster zum Suchen von Übereinstimmungen. |
| replacement | String | Eine Zeichenfolge zum Ersetzen aller Vorkommen des Musters. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) Objekt, um zusätzliche Optionen anzugeben. |

### Rückgabewert

Die Anzahl der vorgenommenen Ersetzungen.

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

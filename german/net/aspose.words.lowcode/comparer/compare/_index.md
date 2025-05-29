---
title: Comparer.Compare
linktitle: Compare
articleTitle: Compare
second_title: Aspose.Words für .NET
description: Vergleichen Sie mühelos zwei Dokumente mit unserer Vergleichsmethode. Speichern Sie Unterschiede und verfolgen Sie Bearbeitungen und Formatänderungen in einer einzigen Ausgabedatei.
type: docs
weight: 20
url: /de/net/aspose.words.lowcode/comparer/compare/
---
## Compare(*string, string, string, string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_4}

Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in der angegebenen Ausgabedatei. Dabei werden Änderungen als eine Reihe von Bearbeitungs- und Formatrevisionen erstellt.

```csharp
public static void Compare(string v1, string v2, string outputFileName, string author, 
    DateTime dateTime, CompareOptions compareOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | String | Das Originaldokument. |
| v2 | String | Das geänderte Dokument. |
| outputFileName | String | Der Name der Ausgabedatei. |
| author | String | Initialen des Autors, die für Überarbeitungen verwendet werden sollen. |
| dateTime | DateTime | Das für Revisionen zu verwendende Datum und die Uhrzeit. |
| compareOptions | CompareOptions | Optionen zum Dokumentenvergleich. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie man Dokumente einfach vergleicht.

```csharp
// Es gibt mehrere Möglichkeiten, Dokumente zu vergleichen:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());

CompareOptions compareOptions = new CompareOptions();
compareOptions.IgnoreCaseChanges = true;
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), compareOptions);
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), compareOptions);
```

### Siehe auch

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Compare(*string, string, string, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_2}

Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in der angegebenen Ausgabedatei im bereitgestellten Speicherformat. Dabei werden Änderungen als eine Reihe von Bearbeitungs- und Formatrevisionen erstellt.

```csharp
public static void Compare(string v1, string v2, string outputFileName, SaveFormat saveFormat, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | String | Das Originaldokument. |
| v2 | String | Das geänderte Dokument. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveFormat | SaveFormat | Das Speicherformat der Ausgabe. |
| author | String | Initialen des Autors, die für Überarbeitungen verwendet werden sollen. |
| dateTime | DateTime | Das für Revisionen zu verwendende Datum und die Uhrzeit. |
| compareOptions | CompareOptions | Optionen zum Dokumentenvergleich. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie man Dokumente einfach vergleicht.

```csharp
// Es gibt mehrere Möglichkeiten, Dokumente zu vergleichen:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());

CompareOptions compareOptions = new CompareOptions();
compareOptions.IgnoreCaseChanges = true;
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), compareOptions);
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), compareOptions);
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Compare(*string, string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_3}

Vergleicht zwei Dokumente mit zusätzlichen Optionen und speichert die Unterschiede in der angegebenen Ausgabedatei im bereitgestellten Speicherformat. Dabei werden Änderungen als eine Reihe von Bearbeitungs- und Formatrevisionen erstellt.

```csharp
public static void Compare(string v1, string v2, string outputFileName, SaveOptions saveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | String | Das Originaldokument. |
| v2 | String | Das geänderte Dokument. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveOptions | SaveOptions | Die Speicheroptionen der Ausgabe. |
| author | String | Initialen des Autors, die für Überarbeitungen verwendet werden sollen. |
| dateTime | DateTime | Das für Revisionen zu verwendende Datum und die Uhrzeit. |
| compareOptions | CompareOptions | Optionen zum Dokumentenvergleich. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Compare(*Stream, Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare}

Vergleicht zwei aus Streams geladene Dokumente mit zusätzlichen Optionen und speichert die Unterschiede im angegebenen Ausgabestream im angegebenen Speicherformat. Dabei werden Änderungen als eine Reihe von Bearbeitungs- und Formatrevisionen erzeugt.

```csharp
public static void Compare(Stream v1, Stream v2, Stream outputStream, SaveFormat saveFormat, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | Stream | Das Originaldokument. |
| v2 | Stream | Das geänderte Dokument. |
| outputStream | Stream | Der Ausgabestream. |
| saveFormat | SaveFormat | Das Speicherformat der Ausgabe. |
| author | String | Initialen des Autors, die für Überarbeitungen verwendet werden sollen. |
| dateTime | DateTime | Das für Revisionen zu verwendende Datum und die Uhrzeit. |
| compareOptions | CompareOptions | Optionen zum Dokumentenvergleich. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

## Beispiele

Zeigt, wie Dokumente aus dem Stream verglichen werden.

```csharp
// Es gibt mehrere Möglichkeiten, Dokumente aus dem Stream zu vergleichen:
using (FileStream firstStreamIn = new FileStream(MyDir + "Table column bookmarks.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Table column bookmarks.doc", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime());

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
        {
            CompareOptions compareOptions = new CompareOptions();
            compareOptions.IgnoreCaseChanges = true;
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime(), compareOptions);
        }
    }
}
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Compare(*Stream, Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_1}

Vergleicht zwei aus Streams geladene Dokumente mit zusätzlichen Optionen und speichert die Unterschiede im angegebenen Ausgabestream im angegebenen Speicherformat. Dabei werden Änderungen als eine Reihe von Bearbeitungs- und Formatrevisionen erzeugt.

```csharp
public static void Compare(Stream v1, Stream v2, Stream outputStream, SaveOptions saveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | Stream | Das Originaldokument. |
| v2 | Stream | Das geänderte Dokument. |
| outputStream | Stream | Der Ausgabestream. |
| saveOptions | SaveOptions | Die Speicheroptionen der Ausgabe. |
| author | String | Initialen des Autors, die für Überarbeitungen verwendet werden sollen. |
| dateTime | DateTime | Das für Revisionen zu verwendende Datum und die Uhrzeit. |
| compareOptions | CompareOptions | Optionen zum Dokumentenvergleich. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

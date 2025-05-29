---
title: MailMerger.Execute
linktitle: Execute
articleTitle: Execute
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihren Arbeitsablauf mit der MailMerger Execute-Methode, indem Sie Daten für einzelne Datensätze mühelos zusammenführen, um die Effizienz und Genauigkeit zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.lowcode/mailmerger/execute/
---
## Execute(*string, string, string[], object[]*) {#execute_14}

Führt einen Serienbriefvorgang für einen einzelnen Datensatz aus.

```csharp
public static void Execute(string inputFileName, string outputFileName, string[] fieldNames, 
    object[] fieldValues)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| fieldNames | String[] | Array von Seriendruckfeldnamen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| fieldValues | Object[] | Array mit Werten, die in die Seriendruckfelder eingefügt werden sollen. Die Anzahl der Elemente in diesem Array muss mit der Anzahl der Elemente in „fieldNames“ übereinstimmen. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie Sie einen Serienbriefvorgang für einen einzelnen Datensatz durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefe zu erstellen:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Siehe auch

* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_8}

Führt einen Serienbriefvorgang für einen einzelnen Datensatz aus.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveFormat | SaveFormat | Das Speicherformat der Ausgabe. |
| fieldNames | String[] | Array von Seriendruckfeldnamen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| fieldValues | Object[] | Array mit Werten, die in die Seriendruckfelder eingefügt werden sollen. Die Anzahl der Elemente in diesem Array muss mit der Anzahl der Elemente in „fieldNames“ übereinstimmen. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie Sie einen Serienbriefvorgang für einen einzelnen Datensatz durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefe zu erstellen:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_11}

Führt einen Serienbriefvorgang für einen einzelnen Datensatz aus.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveOptions | SaveOptions | Die Speicheroptionen der Ausgabe. |
| fieldNames | String[] | Array von Seriendruckfeldnamen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| fieldValues | Object[] | Array mit Werten, die in die Seriendruckfelder eingefügt werden sollen. Die Anzahl der Elemente in diesem Array muss mit der Anzahl der Elemente in „fieldNames“ übereinstimmen. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_2}

Führt einen Serienbriefvorgang für einen einzelnen Datensatz aus.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| outputStream | Stream | Der Ausgabedateistream. |
| saveFormat | SaveFormat | Das Speicherformat der Ausgabe. |
| fieldNames | String[] | Array von Seriendruckfeldnamen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| fieldValues | Object[] | Array mit Werten, die in die Seriendruckfelder eingefügt werden sollen. Die Anzahl der Elemente in diesem Array muss mit der Anzahl der Elemente in „fieldNames“ übereinstimmen. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

## Beispiele

Zeigt, wie ein Serienbriefvorgang für einen einzelnen Datensatz aus dem Stream durchgeführt wird.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefvorgänge mit Dokumenten aus dem Stream durchzuführen:
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, fieldNames, fieldValues);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
    {
        MailMergeOptions mailMergeOptions = new MailMergeOptions();
        mailMergeOptions.TrimWhitespaces = true;
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
    }
}
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_5}

Führt einen Serienbriefvorgang für einen einzelnen Datensatz aus.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| outputStream | Stream | Der Ausgabedateistream. |
| saveOptions | SaveOptions | Die Speicheroptionen der Ausgabe. |
| fieldNames | String[] | Array von Seriendruckfeldnamen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| fieldValues | Object[] | Array mit Werten, die in die Seriendruckfelder eingefügt werden sollen. Die Anzahl der Elemente in diesem Array muss mit der Anzahl der Elemente in „fieldNames“ übereinstimmen. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Execute(*string, string, DataRow*) {#execute_12}

Führt einen Serienbrief aus einer DataRow in das Dokument aus.

```csharp
public static void Execute(string inputFileName, string outputFileName, DataRow dataRow)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| dataRow | DataRow | Zeile mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie Sie einen Serienbriefvorgang aus einer DataRow durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, einen Serienbriefvorgang aus einer DataRow heraus durchzuführen:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.1.docx", dataRow);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.2.docx", SaveFormat.Docx, dataRow);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.3.docx", SaveFormat.Docx, dataRow, new MailMergeOptions() { TrimWhitespaces = true });
```

### Siehe auch

* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_6}

Führt einen Serienbrief aus einer DataRow in das Dokument aus.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveFormat | SaveFormat | Das Speicherformat der Ausgabe. |
| dataRow | DataRow | Zeile mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie Sie einen Serienbriefvorgang aus einer DataRow durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, einen Serienbriefvorgang aus einer DataRow heraus durchzuführen:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.1.docx", dataRow);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.2.docx", SaveFormat.Docx, dataRow);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.3.docx", SaveFormat.Docx, dataRow, new MailMergeOptions() { TrimWhitespaces = true });
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_9}

Führt einen Serienbrief aus einer DataRow in das Dokument aus.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveOptions | SaveOptions | Die Speicheroptionen der Ausgabe. |
| dataRow | DataRow | Zeile mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute}

Führt einen Serienbriefvorgang für einen einzelnen Datensatz aus.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| outputStream | Stream | Der Ausgabedateistream. |
| saveFormat | SaveFormat | Das Speicherformat der Ausgabe. |
| dataRow | DataRow | Zeile mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

## Beispiele

Zeigt, wie Sie einen Serienbriefvorgang aus einer DataRow unter Verwendung von Dokumenten aus dem Stream durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, einen Serienbriefvorgang aus einer DataRow unter Verwendung von Dokumenten aus dem Stream durchzuführen:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamDataRow.1.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, dataRow);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamDataRow.2.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, dataRow, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_3}

Führt einen Serienbriefvorgang für einen einzelnen Datensatz aus.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| outputStream | Stream | Der Ausgabedateistream. |
| saveOptions | SaveOptions | Die Speicheroptionen der Ausgabe. |
| dataRow | DataRow | Zeile mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Execute(*string, string, DataTable*) {#execute_13}

Führt einen Serienbrief aus einer DataTable in das Dokument aus.

```csharp
public static void Execute(string inputFileName, string outputFileName, DataTable dataTable)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| dataTable | DataTable | Tabelle mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie ein Serienbriefvorgang aus einer DataTable heraus durchgeführt wird.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefvorgänge aus einer DataTable heraus durchzuführen:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.1.docx", dataTable);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.2.docx", SaveFormat.Docx, dataTable);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.3.docx", SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Siehe auch

* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_7}

Führt einen Serienbrief aus einer DataRow in das Dokument aus.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveFormat | SaveFormat | Das Speicherformat der Ausgabe. |
| dataTable | DataTable | Tabelle mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

## Beispiele

Zeigt, wie ein Serienbriefvorgang aus einer DataTable heraus durchgeführt wird.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefvorgänge aus einer DataTable heraus durchzuführen:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.1.docx", dataTable);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.2.docx", SaveFormat.Docx, dataTable);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.3.docx", SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_10}

Führt einen Serienbrief aus einer DataRow in das Dokument aus.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| outputFileName | String | Der Name der Ausgabedatei. |
| saveOptions | SaveOptions | Die Speicheroptionen der Ausgabe. |
| dataTable | DataTable | Tabelle mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jedes Teil nach der Regel „outputFile_partIndex.extension“ zu generieren.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne TIFF-Datei mit mehreren Frames gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_1}

Führt einen Serienbriefvorgang für einen einzelnen Datensatz aus.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| outputStream | Stream | Der Ausgabedateistream. |
| saveFormat | SaveFormat | Das Speicherformat der Ausgabe. |
| dataTable | DataTable | Tabelle mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

## Beispiele

Zeigt, wie Sie einen Serienbriefvorgang aus einer DataTable unter Verwendung von Dokumenten aus dem Stream durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefvorgänge aus einer DataTable mithilfe von Dokumenten aus dem Stream durchzuführen:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeDataTable.1.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, dataTable);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeDataTable.2.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_4}

Führt einen Serienbriefvorgang für einen einzelnen Datensatz aus.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| outputStream | Stream | Der Ausgabedateistream. |
| saveOptions | SaveOptions | Die Speicheroptionen der Ausgabe. |
| dataTable | DataTable | Tabelle mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Bemerkungen

Wenn das Ausgabeformat ein Bild ist (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP), wird nur die erste Seite der Ausgabe im angegebenen Stream gespeichert.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelnes TIFF mit mehreren Frames im angegebenen Stream gespeichert.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

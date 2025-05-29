---
title: MailMerger.ExecuteToImages
linktitle: ExecuteToImages
articleTitle: ExecuteToImages
second_title: Aspose.Words für .NET
description: Führen Sie mühelos einen Serienbrief für einzelne Datensätze durch und konvertieren Sie die Ergebnisse mit der MailMerger ExecuteToImages-Methode in qualitativ hochwertige Bilder.
type: docs
weight: 30
url: /de/net/aspose.words.lowcode/mailmerger/executetoimages/
---
## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_5}

Führt einen Serienbriefvorgang für einen einzelnen Datensatz aus und rendert das Ergebnis in Bilder.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| saveOptions | ImageSaveOptions | Die Speicheroptionen der Ausgabe. |
| fieldNames | String[] | Array von Seriendruckfeldnamen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| fieldValues | Object[] | Array mit Werten, die in die Seriendruckfelder eingefügt werden sollen. Die Anzahl der Elemente in diesem Array muss mit der Anzahl der Elemente in „fieldNames“ übereinstimmen. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Beispiele

Zeigt, wie Sie einen Serienbriefvorgang für einen einzelnen Datensatz durchführen und das Ergebnis in Bildern speichern.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefe zu erstellen:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues, mailMergeOptions);
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_2}

Führt einen Serienbriefvorgang für einen einzelnen Datensatz aus und rendert das Ergebnis in Bilder.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| saveOptions | ImageSaveOptions | Die Speicheroptionen der Ausgabe. |
| fieldNames | String[] | Array von Seriendruckfeldnamen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| fieldValues | Object[] | Array mit Werten, die in die Seriendruckfelder eingefügt werden sollen. Die Anzahl der Elemente in diesem Array muss mit der Anzahl der Elemente in „fieldNames“ übereinstimmen. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Beispiele

Zeigt, wie Sie einen Serienbriefvorgang für einen einzelnen Datensatz aus dem Stream durchführen und das Ergebnis in Bildern speichern.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefvorgänge mit Dokumenten aus dem Stream durchzuführen:
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues);

    MailMergeOptions mailMergeOptions = new MailMergeOptions();
    mailMergeOptions.TrimWhitespaces = true;
    images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues, mailMergeOptions);
}
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_3}

Führt einen Serienbrief aus einer DataRow in das Dokument aus und rendert das Ergebnis in Bilder.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| saveOptions | ImageSaveOptions | Die Speicheroptionen der Ausgabe. |
| dataRow | DataRow | Zeile mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Beispiele

Zeigt, wie Sie einen Serienbriefvorgang aus einer DataRow durchführen und das Ergebnis in Bildern speichern.

```csharp
// Es gibt mehrere Möglichkeiten, einen Serienbriefvorgang aus einer DataRow heraus durchzuführen:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataRow);
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataRow, new MailMergeOptions() { TrimWhitespaces = true });
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages}

Führt einen Serienbrief aus einer DataRow in das Dokument aus und rendert das Ergebnis in Bilder.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| saveOptions | ImageSaveOptions | Die Speicheroptionen der Ausgabe. |
| dataRow | DataRow | Zeile mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Beispiele

Zeigt, wie Sie einen Serienbriefvorgang aus einer DataRow mithilfe von Dokumenten aus dem Stream durchführen und das Ergebnis in Bildern speichern.

```csharp
// Es gibt mehrere Möglichkeiten, einen Serienbriefvorgang aus einer DataRow unter Verwendung von Dokumenten aus dem Stream durchzuführen:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataRow);
    images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataRow, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_4}

Führt einen Serienbrief aus einer DataRow in das Dokument aus und rendert das Ergebnis in Bilder.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| saveOptions | ImageSaveOptions | Die Speicheroptionen der Ausgabe. |
| dataTable | DataTable | Tabelle mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Beispiele

Zeigt, wie Sie einen Serienbriefvorgang aus einer Datentabelle durchführen und das Ergebnis in Bildern speichern.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefvorgänge aus einer DataTable heraus durchzuführen:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable);
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_1}

Führt einen Serienbrief aus einer DataRow in das Dokument aus und rendert das Ergebnis in Bilder.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| saveOptions | ImageSaveOptions | Die Speicheroptionen der Ausgabe. |
| dataTable | DataTable | Tabelle mit Daten, die in Seriendruckfelder eingefügt werden sollen. Bei Feldnamen wird die Groß- und Kleinschreibung nicht berücksichtigt. Ein im Dokument nicht gefundener Feldname wird ignoriert. |
| mailMergeOptions | MailMergeOptions | Optionen für Serienbriefe. |

## Beispiele

Zeigt, wie Sie einen Serienbriefvorgang aus einer DataTable mithilfe von Dokumenten aus dem Stream durchführen und in Bildern speichern.

```csharp
// Es gibt mehrere Möglichkeiten, einen Serienbriefvorgang aus einer DataTable mithilfe von Dokumenten aus dem Stream durchzuführen und das Ergebnis in Bildern zu speichern:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable);
    images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

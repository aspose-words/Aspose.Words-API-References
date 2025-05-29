---
title: MailMerger.Execute
linktitle: Execute
articleTitle: Execute
second_title: Aspose.Words för .NET
description: Effektivisera ditt arbetsflöde med MailMerger Execute-metoden, och sammanfoga enkelt data för enskilda poster för att förbättra effektivitet och noggrannhet.
type: docs
weight: 20
url: /sv/net/aspose.words.lowcode/mailmerger/execute/
---
## Execute(*string, string, string[], object[]*) {#execute_14}

Utför en dokumentkopplingsåtgärd för en enskild post.

```csharp
public static void Execute(string inputFileName, string outputFileName, string[] fieldNames, 
    object[] fieldValues)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| fieldNames | String[] | Matris med namn på kopplingsfält. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| fieldValues | Object[] | Matris med värden som ska infogas i kopplingsfälten. Antalet element i denna matris måste vara detsamma som antalet element i fieldNames. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man utför en dokumentkopplingsoperation för en enskild post.

```csharp
// Det finns flera sätt att göra en dokumentkoppling:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Se även

* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_8}

Utför en dokumentkopplingsåtgärd för en enskild post.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| saveFormat | SaveFormat | Utdatas sparformat. |
| fieldNames | String[] | Matris med namn på kopplingsfält. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| fieldValues | Object[] | Matris med värden som ska infogas i kopplingsfälten. Antalet element i denna matris måste vara detsamma som antalet element i fieldNames. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man utför en dokumentkopplingsoperation för en enskild post.

```csharp
// Det finns flera sätt att göra en dokumentkoppling:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_11}

Utför en dokumentkopplingsåtgärd för en enskild post.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| saveOptions | SaveOptions | Utdatas sparalternativ. |
| fieldNames | String[] | Matris med namn på kopplingsfält. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| fieldValues | Object[] | Matris med värden som ska infogas i kopplingsfälten. Antalet element i denna matris måste vara detsamma som antalet element i fieldNames. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_2}

Utför en dokumentkopplingsåtgärd för en enskild post.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Indatafilströmmen. |
| outputStream | Stream | Utdatafilströmmen. |
| saveFormat | SaveFormat | Utdatas sparformat. |
| fieldNames | String[] | Matris med namn på kopplingsfält. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| fieldValues | Object[] | Matris med värden som ska infogas i kopplingsfälten. Antalet element i denna matris måste vara detsamma som antalet element i fieldNames. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata i den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda TIFF med flera bildrutor till den angivna strömmen.

## Exempel

Visar hur man utför en dokumentkopplingsåtgärd för en enskild post från strömmen.

```csharp
// Det finns flera sätt att göra en dokumentkoppling med hjälp av dokument från strömmen:
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

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_5}

Utför en dokumentkopplingsåtgärd för en enskild post.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Indatafilströmmen. |
| outputStream | Stream | Utdatafilströmmen. |
| saveOptions | SaveOptions | Utdatas sparalternativ. |
| fieldNames | String[] | Matris med namn på kopplingsfält. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| fieldValues | Object[] | Matris med värden som ska infogas i kopplingsfälten. Antalet element i denna matris måste vara detsamma som antalet element i fieldNames. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata i den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda TIFF med flera bildrutor till den angivna strömmen.

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*string, string, DataRow*) {#execute_12}

Utför koppling av dokument från en DataRow till dokumentet.

```csharp
public static void Execute(string inputFileName, string outputFileName, DataRow dataRow)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| dataRow | DataRow | Rad som innehåller data som ska infogas i fält för koppling av dokument. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man utför en dokumentkopplingsoperation från en DataRow.

```csharp
// Det finns flera sätt att göra en koppling mellan dokument från en DataRow:
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

### Se även

* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_6}

Utför koppling av dokument från en DataRow till dokumentet.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| saveFormat | SaveFormat | Utdatas sparformat. |
| dataRow | DataRow | Rad som innehåller data som ska infogas i fält för koppling av dokument. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man utför en dokumentkopplingsoperation från en DataRow.

```csharp
// Det finns flera sätt att göra en koppling mellan dokument från en DataRow:
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

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_9}

Utför koppling av dokument från en DataRow till dokumentet.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| saveOptions | SaveOptions | Utdatas sparalternativ. |
| dataRow | DataRow | Rad som innehåller data som ska infogas i fält för koppling av dokument. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute}

Utför en dokumentkopplingsåtgärd för en enskild post.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Indatafilströmmen. |
| outputStream | Stream | Utdatafilströmmen. |
| saveFormat | SaveFormat | Utdatas sparformat. |
| dataRow | DataRow | Rad som innehåller data som ska infogas i fält för koppling av dokument. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata i den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda TIFF med flera bildrutor till den angivna strömmen.

## Exempel

Visar hur man utför en dokumentkopplingsoperation från en DataRow med hjälp av dokument från strömmen.

```csharp
// Det finns flera sätt att göra en dokumentkopplingsoperation från en DataRow med hjälp av dokument från strömmen:
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

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_3}

Utför en dokumentkopplingsåtgärd för en enskild post.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Indatafilströmmen. |
| outputStream | Stream | Utdatafilströmmen. |
| saveOptions | SaveOptions | Utdatas sparalternativ. |
| dataRow | DataRow | Rad som innehåller data som ska infogas i fält för koppling av dokument. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata i den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda TIFF med flera bildrutor till den angivna strömmen.

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*string, string, DataTable*) {#execute_13}

Utför koppling av dokument från en datatabell till dokumentet.

```csharp
public static void Execute(string inputFileName, string outputFileName, DataTable dataTable)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| dataTable | DataTable | Tabell som innehåller data som ska infogas i fält för koppling av dokument. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man utför en dokumentkopplingsoperation från en datatabell.

```csharp
// Det finns flera sätt att göra en dokumentkopplingsoperation från en datatabell:
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

### Se även

* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_7}

Utför koppling av dokument från en DataRow till dokumentet.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| saveFormat | SaveFormat | Utdatas sparformat. |
| dataTable | DataTable | Tabell som innehåller data som ska infogas i fält för koppling av dokument. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man utför en dokumentkopplingsoperation från en datatabell.

```csharp
// Det finns flera sätt att göra en dokumentkopplingsoperation från en datatabell:
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

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_10}

Utför koppling av dokument från en DataRow till dokumentet.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| saveOptions | SaveOptions | Utdatas sparalternativ. |
| dataTable | DataTable | Tabell som innehåller data som ska infogas i fält för koppling av dokument. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_1}

Utför en dokumentkopplingsåtgärd för en enskild post.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Indatafilströmmen. |
| outputStream | Stream | Utdatafilströmmen. |
| saveFormat | SaveFormat | Utdatas sparformat. |
| dataTable | DataTable | Tabell som innehåller data som ska infogas i fält för koppling av dokument. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata i den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda TIFF med flera bildrutor till den angivna strömmen.

## Exempel

Visar hur man utför en dokumentkopplingsoperation från en datatabell med hjälp av dokument från strömmen.

```csharp
// Det finns flera sätt att göra en dokumentkopplingsoperation från en datatabell med hjälp av dokument från strömmen:
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

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_4}

Utför en dokumentkopplingsåtgärd för en enskild post.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Indatafilströmmen. |
| outputStream | Stream | Utdatafilströmmen. |
| saveOptions | SaveOptions | Utdatas sparalternativ. |
| dataTable | DataTable | Tabell som innehåller data som ska infogas i fält för koppling av dokument. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata i den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda TIFF med flera bildrutor till den angivna strömmen.

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

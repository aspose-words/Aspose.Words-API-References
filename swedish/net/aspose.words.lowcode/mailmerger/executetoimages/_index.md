---
title: MailMerger.ExecuteToImages
linktitle: ExecuteToImages
articleTitle: ExecuteToImages
second_title: Aspose.Words för .NET
description: Utför enkelt en dokumentkoppling för enskilda poster och konvertera resultaten till högkvalitativa bilder med MailMerger ExecuteToImages-metoden.
type: docs
weight: 30
url: /sv/net/aspose.words.lowcode/mailmerger/executetoimages/
---
## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_5}

Utför en dokumentkopplingsoperation för en enskild post och renderar resultatet som bilder.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| saveOptions | ImageSaveOptions | Utdatas sparalternativ. |
| fieldNames | String[] | Matris med namn på kopplingsfält. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| fieldValues | Object[] | Matris med värden som ska infogas i kopplingsfälten. Antalet element i denna matris måste vara detsamma som antalet element i fieldNames. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Exempel

Visar hur man utför en dokumentkopplingsoperation för en enskild post och sparar resultatet som bilder.

```csharp
// Det finns flera sätt att göra en dokumentkoppling:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues, mailMergeOptions);
```

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_2}

Utför en dokumentkopplingsoperation för en enskild post och renderar resultatet som bilder.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Indatafilströmmen. |
| saveOptions | ImageSaveOptions | Utdatas sparalternativ. |
| fieldNames | String[] | Matris med namn på kopplingsfält. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| fieldValues | Object[] | Matris med värden som ska infogas i kopplingsfälten. Antalet element i denna matris måste vara detsamma som antalet element i fieldNames. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Exempel

Visar hur man utför en dokumentkopplingsoperation för en enskild post från strömmen och sparar resultatet till bilder.

```csharp
// Det finns flera sätt att göra en dokumentkoppling med hjälp av dokument från strömmen:
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

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_3}

Utför dokumentkoppling från en DataRow till dokumentet och renderar resultatet som bilder.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| saveOptions | ImageSaveOptions | Utdatas sparalternativ. |
| dataRow | DataRow | Rad som innehåller data som ska infogas i fält för koppling av dokument. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Exempel

Visar hur man utför en dokumentkopplingsoperation från en DataRow och sparar resultatet till bilder.

```csharp
// Det finns flera sätt att göra en koppling mellan dokument från en DataRow:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataRow);
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataRow, new MailMergeOptions() { TrimWhitespaces = true });
```

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages}

Utför dokumentkoppling från en DataRow till dokumentet och renderar resultatet som bilder.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Indatafilströmmen. |
| saveOptions | ImageSaveOptions | Utdatas sparalternativ. |
| dataRow | DataRow | Rad som innehåller data som ska infogas i fält för koppling av dokument. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Exempel

Visar hur man utför en dokumentkopplingsoperation från en DataRow med hjälp av dokument från strömmen och sparar resultatet till bilder.

```csharp
// Det finns flera sätt att göra en dokumentkopplingsoperation från en DataRow med hjälp av dokument från strömmen:
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

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_4}

Utför dokumentkoppling från en DataRow till dokumentet och renderar resultatet som bilder.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| saveOptions | ImageSaveOptions | Utdatas sparalternativ. |
| dataTable | DataTable | Tabell som innehåller data som ska infogas i fält för koppling av dokument. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Exempel

Visar hur man utför en dokumentkopplingsoperation från en datatabell och sparar resultatet till bilder.

```csharp
// Det finns flera sätt att göra en dokumentkopplingsoperation från en datatabell:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable);
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_1}

Utför dokumentkoppling från en DataRow till dokumentet och renderar resultatet som bilder.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Indatafilströmmen. |
| saveOptions | ImageSaveOptions | Utdatas sparalternativ. |
| dataTable | DataTable | Tabell som innehåller data som ska infogas i fält för koppling av dokument. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Exempel

Visar hur man utför en dokumentkopplingsoperation från en datatabell med hjälp av dokument från strömmen och sparar till bilder.

```csharp
// Det finns flera sätt att göra en dokumentkopplingsoperation från en datatabell med hjälp av dokument från strömmen och spara resultatet till bilder:
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

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---
title: MailMerger.ExecuteWithRegionsToImages
linktitle: ExecuteWithRegionsToImages
articleTitle: ExecuteWithRegionsToImages
second_title: Aspose.Words för .NET
description: Sammanfoga enkelt data från en datatabell till dokument med MailMerger ExecuteWithRegionsToImages och förvandla ditt innehåll till fantastiska bilder.
type: docs
weight: 50
url: /sv/net/aspose.words.lowcode/mailmerger/executewithregionstoimages/
---
## ExecuteWithRegionsToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages_3}

Utför dokumentkoppling från en datatabell till dokumentet med områden för dokumentkoppling och renderar resultatet som bilder.

```csharp
public static Stream[] ExecuteWithRegionsToImages(string inputFileName, 
    ImageSaveOptions saveOptions, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| saveOptions | ImageSaveOptions | Utdatas sparalternativ. |
| dataTable | DataTable | Tabell som innehåller data som ska infogas i fält för koppling av dokument. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Exempel

Visar hur man gör en dokumentkoppling med regioner från en datatabell och sparar resultatet till bilder.

```csharp
// Det finns flera sätt att göra dokumentkoppling med regioner från en datatabell:
string doc = MyDir + "Mail merge with regions.docx";

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

Stream[] images = MailMerger.ExecuteWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable);
images = MailMerger.ExecuteWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## ExecuteWithRegionsToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages_1}

Utför dokumentkoppling från en datatabell till dokumentet med områden för dokumentkoppling och renderar resultatet som bilder.

```csharp
public static Stream[] ExecuteWithRegionsToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Indatafilströmmen. |
| saveOptions | ImageSaveOptions | Utdatas sparalternativ. |
| dataTable | DataTable | Tabell som innehåller data som ska infogas i fält för koppling av dokument. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas ignoreras det. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Exempel

Visar hur man gör dokumentkoppling med regioner från en datatabell med hjälp av dokument från strömmen och sparar resultatet till bilder.

```csharp
// Det finns flera sätt att göra dokumentkoppling med regioner från en datatabell med hjälp av dokument från strömmen:
DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable);
    images = MailMerger.ExecuteWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## ExecuteWithRegionsToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages_2}

Utför koppling av dokument från en datauppsättning till dokumentet med kopplingsområden och renderar resultatet som bilder.

```csharp
public static Stream[] ExecuteWithRegionsToImages(string inputFileName, 
    ImageSaveOptions saveOptions, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| saveOptions | ImageSaveOptions | Utdatas sparalternativ. |
| dataSet | DataSet | Dataset som innehåller data som ska infogas i fält för koppling av dokument. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Exempel

Visar hur man gör en dokumentkoppling med regioner från en datauppsättning och sparar resultatet till bilder.

```csharp
// Det finns flera sätt att göra dokumentkoppling med regioner från en datauppsättning:
string doc = MyDir + "Mail merge with regions data set.docx";

DataTable tableCustomers = new DataTable("Customers");
tableCustomers.Columns.Add("CustomerID");
tableCustomers.Columns.Add("CustomerName");
tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

DataTable tableOrders = new DataTable("Orders");
tableOrders.Columns.Add("CustomerID");
tableOrders.Columns.Add("ItemName");
tableOrders.Columns.Add("Quantity");
tableOrders.Rows.Add(new object[] { 1, "Hawaiian", 2 });
tableOrders.Rows.Add(new object[] { 2, "Pepperoni", 1 });
tableOrders.Rows.Add(new object[] { 2, "Chicago", 1 });

DataSet dataSet = new DataSet();
dataSet.Tables.Add(tableCustomers);
dataSet.Tables.Add(tableOrders);
dataSet.Relations.Add(tableCustomers.Columns["CustomerID"], tableOrders.Columns["CustomerID"]);

Stream[] images = MailMerger.ExecuteWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataSet);
images = MailMerger.ExecuteWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataSet, new MailMergeOptions() { TrimWhitespaces = true });
```

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## ExecuteWithRegionsToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages}

Utför koppling av dokument från en datauppsättning till dokumentet med kopplingsområden och renderar resultatet som bilder.

```csharp
public static Stream[] ExecuteWithRegionsToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Indatafilströmmen. |
| saveOptions | ImageSaveOptions | Utdatas sparalternativ. |
| dataSet | DataSet | Dataset som innehåller data som ska infogas i fält för koppling av dokument. |
| mailMergeOptions | MailMergeOptions | Alternativ för dokumentkoppling. |

## Exempel

Visar hur man gör dokumentkoppling med regioner från en datauppsättning med hjälp av dokument från strömmen och sparar resultatet till bilder.

```csharp
// Det finns flera sätt att göra dokumentkoppling med regioner från en datauppsättning med hjälp av dokument från dataströmmen:
DataTable tableCustomers = new DataTable("Customers");
tableCustomers.Columns.Add("CustomerID");
tableCustomers.Columns.Add("CustomerName");
tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

DataTable tableOrders = new DataTable("Orders");
tableOrders.Columns.Add("CustomerID");
tableOrders.Columns.Add("ItemName");
tableOrders.Columns.Add("Quantity");
tableOrders.Rows.Add(new object[] { 1, "Hawaiian", 2 });
tableOrders.Rows.Add(new object[] { 2, "Pepperoni", 1 });
tableOrders.Rows.Add(new object[] { 2, "Chicago", 1 });

DataSet dataSet = new DataSet();
dataSet.Tables.Add(tableCustomers);
dataSet.Tables.Add(tableOrders);
dataSet.Relations.Add(tableCustomers.Columns["CustomerID"], tableOrders.Columns["CustomerID"]);

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataSet);
    images = MailMerger.ExecuteWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataSet, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

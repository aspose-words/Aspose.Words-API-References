---
title: MailMerger.ExecuteWithRegionsToImages
linktitle: ExecuteWithRegionsToImages
articleTitle: ExecuteWithRegionsToImages
second_title: .NET için Aspose.Words
description: MailMerger ExecuteWithRegionsToImages ile bir DataTable'daki verileri zahmetsizce belgelere birleştirin ve içeriğinizi çarpıcı görüntülere dönüştürün.
type: docs
weight: 50
url: /tr/net/aspose.words.lowcode/mailmerger/executewithregionstoimages/
---
## ExecuteWithRegionsToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages_3}

Bir DataTable'dan belgeye posta birleştirme işlemini posta birleştirme bölgeleriyle gerçekleştirir ve sonucu resimlere dönüştürür.

```csharp
public static Stream[] ExecuteWithRegionsToImages(string inputFileName, 
    ImageSaveOptions saveOptions, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| saveOptions | ImageSaveOptions | Çıktının kaydetme seçenekleri. |
| dataTable | DataTable | Posta birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Örnekler

Bir DataTable'dan bölgelerle posta birleştirme işleminin nasıl yapılacağını ve sonucun resimlere nasıl kaydedileceğini gösterir.

```csharp
// DataTable'dan bölgelerle posta birleştirme işlemini yapmanın birkaç yolu vardır:
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

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegionsToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages_1}

Bir DataTable'dan belgeye posta birleştirme işlemini posta birleştirme bölgeleriyle gerçekleştirir ve sonucu resimlere dönüştürür.

```csharp
public static Stream[] ExecuteWithRegionsToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| saveOptions | ImageSaveOptions | Çıktının kaydetme seçenekleri. |
| dataTable | DataTable | Posta birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Örnekler

Akıştaki belgeleri kullanarak bir DataTable'dan bölgelerle posta birleştirme işleminin nasıl yapılacağını ve sonuçların resimlere nasıl kaydedileceğini gösterir.

```csharp
// Akıştaki belgeleri kullanarak bir DataTable'dan bölgelerle posta birleştirme işlemini yapmanın birkaç yolu vardır:
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

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegionsToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages_2}

Bir DataSet'ten belgeye posta birleştirme işlemini posta birleştirme bölgeleriyle gerçekleştirir ve sonucu resimlere dönüştürür.

```csharp
public static Stream[] ExecuteWithRegionsToImages(string inputFileName, 
    ImageSaveOptions saveOptions, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| saveOptions | ImageSaveOptions | Çıktının kaydetme seçenekleri. |
| dataSet | DataSet | Posta birleştirme alanlarına eklenecek verileri içeren DataSet. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Örnekler

Bir DataSet'ten bölgelerle posta birleştirme işleminin nasıl yapılacağını ve sonucun resimlere nasıl kaydedileceğini gösterir.

```csharp
// Bir DataSet'ten bölgelerle posta birleştirme işlemini yapmanın birkaç yolu vardır:
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

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegionsToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages}

Bir DataSet'ten belgeye posta birleştirme işlemini posta birleştirme bölgeleriyle gerçekleştirir ve sonucu resimlere dönüştürür.

```csharp
public static Stream[] ExecuteWithRegionsToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| saveOptions | ImageSaveOptions | Çıktının kaydetme seçenekleri. |
| dataSet | DataSet | Posta birleştirme alanlarına eklenecek verileri içeren DataSet. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Örnekler

Akıştaki belgeleri kullanarak bir DataSet'ten bölgelerle posta birleştirme işleminin nasıl yapılacağını ve sonuçların resimlere nasıl kaydedileceğini gösterir.

```csharp
// Akıştaki belgeleri kullanarak bir DataSet'ten bölgelerle posta birleştirme işlemini yapmanın birkaç yolu vardır:
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

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

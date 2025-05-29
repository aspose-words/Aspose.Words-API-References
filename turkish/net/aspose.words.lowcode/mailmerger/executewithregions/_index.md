---
title: MailMerger.ExecuteWithRegions
linktitle: ExecuteWithRegions
articleTitle: ExecuteWithRegions
second_title: .NET için Aspose.Words
description: MailMerger'ın ExecuteWithRegions yöntemiyle belge oluşturmanızı kolaylaştırın. Özelleştirilebilir bölgeleri kullanarak DataTable'ları zahmetsizce belgelere birleştirin.
type: docs
weight: 40
url: /tr/net/aspose.words.lowcode/mailmerger/executewithregions/
---
## ExecuteWithRegions(*string, string, DataTable*) {#executewithregions_9}

Bir DataTable'dan bir belgeye posta birleştirme işlemini posta birleştirme bölgeleriyle gerçekleştirir.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    DataTable dataTable)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| dataTable | DataTable | Posta birleştirme işlemi için veri kaynağı. Tablonun TableName özelliğinin ayarlanmış olması gerekir. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

DataTable'dan bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// DataTable'dan bölgelerle posta birleştirme işlemini yapmanın birkaç yolu vardır:
string doc = MyDir + "Mail merge with regions.docx";

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.1.docx", dataTable);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.2.docx", SaveFormat.Docx, dataTable);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.3.docx", SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Ayrıca bakınız

* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_5}

Bir DataTable'dan bir belgeye posta birleştirme işlemini posta birleştirme bölgeleriyle gerçekleştirir.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveFormat saveFormat, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveFormat | SaveFormat | Çıktının kaydedileceği format. |
| dataTable | DataTable | Posta birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

DataTable'dan bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// DataTable'dan bölgelerle posta birleştirme işlemini yapmanın birkaç yolu vardır:
string doc = MyDir + "Mail merge with regions.docx";

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.1.docx", dataTable);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.2.docx", SaveFormat.Docx, dataTable);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.3.docx", SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_7}

Bir DataTable'dan bir belgeye posta birleştirme işlemini posta birleştirme bölgeleriyle gerçekleştirir.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveOptions | SaveOptions | Çıktının kaydetme seçenekleri. |
| dataTable | DataTable | Posta birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_1}

Tek bir kayıt için bir posta birleştirme işlemi gerçekleştirir.

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| outputStream | Stream | Çıktı dosya akışı. |
| saveFormat | SaveFormat | Çıktının kaydedileceği format. |
| dataTable | DataTable | Posta birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Örnekler

Akıştaki belgeleri kullanarak bir DataTable'dan bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

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
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamWithRegionsDataTable.1.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.ExecuteWithRegions(streamIn, streamOut, SaveFormat.Docx, dataTable);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamWithRegionsDataTable.2.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.ExecuteWithRegions(streamIn, streamOut, SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_3}

Tek bir kayıt için bir posta birleştirme işlemi gerçekleştirir.

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| outputStream | Stream | Çıktı dosya akışı. |
| saveOptions | SaveOptions | Çıktının kaydetme seçenekleri. |
| dataTable | DataTable | Posta birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, DataSet*) {#executewithregions_8}

Bir Veri Kümesinden bir belgeye posta birleştirme işlemini posta birleştirme bölgeleri ile gerçekleştirir.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, DataSet dataSet)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| dataSet | DataSet | Posta birleştirme alanlarına eklenecek verileri içeren DataSet. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Bir DataSet'ten bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

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

MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.1.docx", dataSet);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.2.docx", SaveFormat.Docx, dataSet);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.3.docx", SaveFormat.Docx, dataSet, new MailMergeOptions() { TrimWhitespaces = true });
```

### Ayrıca bakınız

* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_4}

Bir Veri Kümesinden belgeye posta birleştirme işlemini posta birleştirme bölgeleriyle gerçekleştirir.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveFormat saveFormat, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveFormat | SaveFormat | Çıktının kaydedileceği format. |
| dataSet | DataSet | Posta birleştirme alanlarına eklenecek verileri içeren DataSet. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Bir DataSet'ten bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

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

MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.1.docx", dataSet);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.2.docx", SaveFormat.Docx, dataSet);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.3.docx", SaveFormat.Docx, dataSet, new MailMergeOptions() { TrimWhitespaces = true });
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_6}

Bir Veri Kümesinden belgeye posta birleştirme işlemini posta birleştirme bölgeleriyle gerçekleştirir.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveOptions | SaveOptions | Çıktının kaydetme seçenekleri. |
| dataSet | DataSet | Posta birleştirme alanlarına eklenecek verileri içeren DataSet. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions}

Bir Veri Kümesinden belgeye posta birleştirme işlemini posta birleştirme bölgeleriyle gerçekleştirir.

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| outputStream | Stream | Çıktı dosya akışı. |
| saveFormat | SaveFormat | Çıktının kaydedileceği format. |
| dataSet | DataSet | Posta birleştirme alanlarına eklenecek verileri içeren DataSet. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Örnekler

Akıştaki belgeleri kullanarak bir DataSet'ten bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

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
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamWithRegionsDataTable.1.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.ExecuteWithRegions(streamIn, streamOut, SaveFormat.Docx, dataSet);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamWithRegionsDataTable.2.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.ExecuteWithRegions(streamIn, streamOut, SaveFormat.Docx, dataSet, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_2}

Bir Veri Kümesinden belgeye posta birleştirme işlemini posta birleştirme bölgeleriyle gerçekleştirir.

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| outputStream | Stream | Çıktı dosya akışı. |
| saveOptions | SaveOptions | Çıktının kaydetme seçenekleri. |
| dataSet | DataSet | Posta birleştirme alanlarına eklenecek verileri içeren DataSet. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

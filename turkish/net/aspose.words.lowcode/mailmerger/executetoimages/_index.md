---
title: MailMerger.ExecuteToImages
linktitle: ExecuteToImages
articleTitle: ExecuteToImages
second_title: .NET için Aspose.Words
description: MailMerger ExecuteToImages metodunu kullanarak tek tek kayıtlar için e-posta birleştirme işlemini zahmetsizce gerçekleştirin ve sonuçları yüksek kaliteli görsellere dönüştürün.
type: docs
weight: 30
url: /tr/net/aspose.words.lowcode/mailmerger/executetoimages/
---
## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_5}

Tek bir kayıt için bir posta birleştirme işlemi gerçekleştirir ve sonucu resimlere dönüştürür.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| saveOptions | ImageSaveOptions | Çıktının kaydetme seçenekleri. |
| fieldNames | String[] | Birleştirme alanı adları dizisi. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| fieldValues | Object[] | Birleştirme alanlarına eklenecek değerler dizisi. Bu dizideki öğe sayısı fieldNames'deki öğe sayısıyla aynı olmalıdır. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Örnekler

Tek bir kayıt için birleştirme işleminin nasıl yapılacağını ve sonucun resimlere nasıl kaydedileceğini gösterir.

```csharp
// Posta birleştirme işlemini yapmanın birkaç yolu vardır:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues, mailMergeOptions);
```

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_2}

Tek bir kayıt için bir posta birleştirme işlemi gerçekleştirir ve sonucu resimlere dönüştürür.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| saveOptions | ImageSaveOptions | Çıktının kaydetme seçenekleri. |
| fieldNames | String[] | Birleştirme alanı adları dizisi. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| fieldValues | Object[] | Birleştirme alanlarına eklenecek değerler dizisi. Bu dizideki öğe sayısı fieldNames'deki öğe sayısıyla aynı olmalıdır. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Örnekler

Akıştaki tek bir kayıt için birleştirme işleminin nasıl yapılacağını ve sonucun resimlere nasıl kaydedileceğini gösterir.

```csharp
// Akıştaki belgeleri kullanarak posta birleştirme işlemini yapmanın birkaç yolu vardır:
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

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_3}

Bir DataRow'dan belgeye posta birleştirme gerçekleştirir ve sonucu images'a işler.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| saveOptions | ImageSaveOptions | Çıktının kaydetme seçenekleri. |
| dataRow | DataRow | Posta birleştirme alanlarına eklenecek verileri içeren satır. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Örnekler

DataRow'dan posta birleştirme işleminin nasıl yapılacağını ve sonucun resimlere nasıl kaydedileceğini gösterir.

```csharp
// DataRow'dan posta birleştirme işlemini yapmanın birkaç yolu vardır:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataRow);
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataRow, new MailMergeOptions() { TrimWhitespaces = true });
```

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages}

Bir DataRow'dan belgeye posta birleştirme gerçekleştirir ve sonucu images'a işler.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| saveOptions | ImageSaveOptions | Çıktının kaydetme seçenekleri. |
| dataRow | DataRow | Posta birleştirme alanlarına eklenecek verileri içeren satır. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Örnekler

Akıştaki belgeleri kullanarak bir DataRow'dan posta birleştirme işleminin nasıl yapılacağını ve sonucun resimlere nasıl kaydedileceğini gösterir.

```csharp
// Akıştaki belgeleri kullanarak bir DataRow'dan posta birleştirme işlemi yapmanın birkaç yolu vardır:
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

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_4}

Bir DataRow'dan belgeye posta birleştirme gerçekleştirir ve sonucu images'a işler.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| saveOptions | ImageSaveOptions | Çıktının kaydetme seçenekleri. |
| dataTable | DataTable | Posta birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Örnekler

DataTable'dan birleştirme işleminin nasıl yapılacağını ve sonuçların resimlere nasıl kaydedileceğini gösterir.

```csharp
// DataTable'dan posta birleştirme işlemini yapmanın birkaç yolu vardır:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable);
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_1}

Bir DataRow'dan belgeye posta birleştirme gerçekleştirir ve sonucu images'a işler.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| saveOptions | ImageSaveOptions | Çıktının kaydetme seçenekleri. |
| dataTable | DataTable | Posta birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Örnekler

Akıştaki belgeleri kullanarak bir DataTable'dan posta birleştirme işleminin nasıl yapılacağını ve resimlere nasıl kaydedileceğini gösterir.

```csharp
// Akıştaki belgeleri kullanarak bir DataTable'dan posta birleştirme işlemi yapmanın ve sonuçları resimlere kaydetmenin birkaç yolu vardır:
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

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

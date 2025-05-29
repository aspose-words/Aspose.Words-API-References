---
title: MailMerger.Execute
linktitle: Execute
articleTitle: Execute
second_title: .NET için Aspose.Words
description: MailMerger Execute yöntemi ile iş akışınızı kolaylaştırın; verimliliği ve doğruluğu artırmak için tek kayıtlara ait verileri zahmetsizce birleştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.lowcode/mailmerger/execute/
---
## Execute(*string, string, string[], object[]*) {#execute_14}

Tek bir kayıt için bir posta birleştirme işlemi gerçekleştirir.

```csharp
public static void Execute(string inputFileName, string outputFileName, string[] fieldNames, 
    object[] fieldValues)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| fieldNames | String[] | Birleştirme alanı adları dizisi. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| fieldValues | Object[] | Birleştirme alanlarına eklenecek değerler dizisi. Bu dizideki öğe sayısı fieldNames'deki öğe sayısıyla aynı olmalıdır. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Posta birleştirme işlemini yapmanın birkaç yolu vardır:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Ayrıca bakınız

* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_8}

Tek bir kayıt için bir posta birleştirme işlemi gerçekleştirir.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveFormat | SaveFormat | Çıktının kaydedileceği format. |
| fieldNames | String[] | Birleştirme alanı adları dizisi. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| fieldValues | Object[] | Birleştirme alanlarına eklenecek değerler dizisi. Bu dizideki öğe sayısı fieldNames'deki öğe sayısıyla aynı olmalıdır. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Posta birleştirme işlemini yapmanın birkaç yolu vardır:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_11}

Tek bir kayıt için bir posta birleştirme işlemi gerçekleştirir.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveOptions | SaveOptions | Çıktının kaydetme seçenekleri. |
| fieldNames | String[] | Birleştirme alanı adları dizisi. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| fieldValues | Object[] | Birleştirme alanlarına eklenecek değerler dizisi. Bu dizideki öğe sayısı fieldNames'deki öğe sayısıyla aynı olmalıdır. |
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

## Execute(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_2}

Tek bir kayıt için bir posta birleştirme işlemi gerçekleştirir.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| outputStream | Stream | Çıktı dosya akışı. |
| saveFormat | SaveFormat | Çıktının kaydedileceği format. |
| fieldNames | String[] | Birleştirme alanı adları dizisi. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| fieldValues | Object[] | Birleştirme alanlarına eklenecek değerler dizisi. Bu dizideki öğe sayısı fieldNames'deki öğe sayısıyla aynı olmalıdır. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Örnekler

Akıştaki tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Akıştaki belgeleri kullanarak posta birleştirme işlemini yapmanın birkaç yolu vardır:
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

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_5}

Tek bir kayıt için bir posta birleştirme işlemi gerçekleştirir.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| outputStream | Stream | Çıktı dosya akışı. |
| saveOptions | SaveOptions | Çıktının kaydetme seçenekleri. |
| fieldNames | String[] | Birleştirme alanı adları dizisi. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| fieldValues | Object[] | Birleştirme alanlarına eklenecek değerler dizisi. Bu dizideki öğe sayısı fieldNames'deki öğe sayısıyla aynı olmalıdır. |
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

## Execute(*string, string, DataRow*) {#execute_12}

Bir DataRow'dan belgeye posta birleştirme işlemini gerçekleştirir.

```csharp
public static void Execute(string inputFileName, string outputFileName, DataRow dataRow)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| dataRow | DataRow | Posta birleştirme alanlarına eklenecek verileri içeren satır. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

DataRow'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// DataRow'dan posta birleştirme işlemini yapmanın birkaç yolu vardır:
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

### Ayrıca bakınız

* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_6}

Bir DataRow'dan belgeye posta birleştirme işlemini gerçekleştirir.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveFormat | SaveFormat | Çıktının kaydedileceği format. |
| dataRow | DataRow | Posta birleştirme alanlarına eklenecek verileri içeren satır. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

DataRow'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// DataRow'dan posta birleştirme işlemini yapmanın birkaç yolu vardır:
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

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_9}

Bir DataRow'dan belgeye posta birleştirme işlemini gerçekleştirir.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveOptions | SaveOptions | Çıktının kaydetme seçenekleri. |
| dataRow | DataRow | Posta birleştirme alanlarına eklenecek verileri içeren satır. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
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

## Execute(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute}

Tek bir kayıt için bir posta birleştirme işlemi gerçekleştirir.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| outputStream | Stream | Çıktı dosya akışı. |
| saveFormat | SaveFormat | Çıktının kaydedileceği format. |
| dataRow | DataRow | Posta birleştirme alanlarına eklenecek verileri içeren satır. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
| mailMergeOptions | MailMergeOptions | Posta birleştirme seçenekleri. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Örnekler

Akıştaki belgeleri kullanarak bir DataRow'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Akıştaki belgeleri kullanarak bir DataRow'dan posta birleştirme işlemi yapmanın birkaç yolu vardır:
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

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_3}

Tek bir kayıt için bir posta birleştirme işlemi gerçekleştirir.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| outputStream | Stream | Çıktı dosya akışı. |
| saveOptions | SaveOptions | Çıktının kaydetme seçenekleri. |
| dataRow | DataRow | Posta birleştirme alanlarına eklenecek verileri içeren satır. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |
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

## Execute(*string, string, DataTable*) {#execute_13}

Bir DataTable'dan belgeye posta birleştirme işlemini gerçekleştirir.

```csharp
public static void Execute(string inputFileName, string outputFileName, DataTable dataTable)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| dataTable | DataTable | Posta birleştirme alanlarına eklenecek verileri içeren tablo. Alan adları büyük/küçük harfe duyarlı değildir. Belgede bulunmayan bir alan adıyla karşılaşılırsa, bu ad yoksayılır. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

DataTable'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// DataTable'dan posta birleştirme işlemini yapmanın birkaç yolu vardır:
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

### Ayrıca bakınız

* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_7}

Bir DataRow'dan belgeye posta birleştirme işlemini gerçekleştirir.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
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

DataTable'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// DataTable'dan posta birleştirme işlemini yapmanın birkaç yolu vardır:
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

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_10}

Bir DataRow'dan belgeye posta birleştirme işlemini gerçekleştirir.

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
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

## Execute(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_1}

Tek bir kayıt için bir posta birleştirme işlemi gerçekleştirir.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
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

Akıştaki belgeleri kullanarak bir DataTable'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Akıştaki belgeleri kullanarak bir DataTable'dan posta birleştirme işlemi yapmanın birkaç yolu vardır:
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

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_4}

Tek bir kayıt için bir posta birleştirme işlemi gerçekleştirir.

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
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

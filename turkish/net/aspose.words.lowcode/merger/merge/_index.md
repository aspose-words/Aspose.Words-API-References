---
title: Merger.Merge
linktitle: Merge
articleTitle: Merge
second_title: .NET için Aspose.Words
description: Birleştirme Birleştirme yöntemimizle birden fazla belgeyi zahmetsizce tek bir belgede birleştirin. İş akışınızı bugün özelleştirilebilir dosya seçenekleriyle kolaylaştırın!
type: docs
weight: 20
url: /tr/net/aspose.words.lowcode/merger/merge/
---
## Merge(*string, string[]*) {#merge_8}

Belirtilen input ve çıktı dosya adlarını kullanarak verilen giriş belgelerini tek bir çıktı belgesinde birleştirirKeepSourceFormatting .

```csharp
public static void Merge(string outputFile, string[] inputFiles)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| outputFile | String | Çıktı dosyasının adı. |
| inputFiles | String[] | Giriş dosya adları. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Belgeleri birleştirmenin birkaç yolu vardır:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Ayrıca bakınız

* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Merge(*string, string[], [SaveFormat](../../../aspose.words/saveformat/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_10}

Belirtilen giriş-çıkış dosya adlarını ve son belge biçimini kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir.

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveFormat saveFormat, 
    MergeFormatMode mergeFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| outputFile | String | Çıktı dosyasının adı. |
| inputFiles | String[] | Giriş dosya adları. |
| saveFormat | SaveFormat | Kaydetme biçimi. |
| mergeFormatMode | MergeFormatMode | Çakışan biçimlendirmelerin nasıl birleştirileceğini belirtir. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Belgeleri birleştirmenin birkaç yolu vardır:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Merge(*string, string[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_11}

Belirtilen giriş-çıkış dosya adlarını ve kaydetme seçeneklerini kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir.

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| outputFile | String | Çıktı dosyasının adı. |
| inputFiles | String[] | Giriş dosya adları. |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |
| mergeFormatMode | MergeFormatMode | Çakışan biçimlendirmelerin nasıl birleştirileceğini belirtir. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Belgeleri birleştirmenin birkaç yolu vardır:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Merge(*string, string[], LoadOptions[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_9}

Belirtilen giriş-çıkış dosya adlarını ve kaydetme seçeneklerini kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir.

```csharp
public static void Merge(string outputFile, string[] inputFiles, LoadOptions[] loadOptions, 
    SaveOptions saveOptions, MergeFormatMode mergeFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| outputFile | String | Çıktı dosyasının adı. |
| inputFiles | String[] | Giriş dosya adları. |
| loadOptions | LoadOptions[] | Giriş dosyaları için yükleme seçenekleri. |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |
| mergeFormatMode | MergeFormatMode | Çakışan biçimlendirmelerin nasıl birleştirileceğini belirtir. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Belgeleri birleştirmenin birkaç yolu vardır:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Ayrıca bakınız

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Merge(*string[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_4}

Verilen giriş belgelerini tek bir belgede birleştirir ve döndürür[`Document`](../../../aspose.words/document/) son belgenin örneği.

```csharp
public static Document Merge(string[] inputFiles, MergeFormatMode mergeFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFiles | String[] | Giriş dosya adları. |
| mergeFormatMode | MergeFormatMode | Çakışan biçimlendirmelerin nasıl birleştirileceğini belirtir. |

## Örnekler

Belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Belgeleri birleştirmenin birkaç yolu vardır:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Merge(*string[], LoadOptions[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_3}

Verilen giriş belgelerini tek bir belgede birleştirir ve döndürür[`Document`](../../../aspose.words/document/) son belgenin örneği.

```csharp
public static Document Merge(string[] inputFiles, LoadOptions[] loadOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFiles | String[] | Giriş dosya adları. |
| loadOptions | LoadOptions[] | Giriş dosyaları için yükleme seçenekleri. |
| mergeFormatMode | MergeFormatMode | Çakışan biçimlendirmelerin nasıl birleştirileceğini belirtir. |

## Örnekler

Belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Belgeleri birleştirmenin birkaç yolu vardır:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Merge(*Document[], [MergeFormatMode](../../mergeformatmode/)*) {#merge}

Verilen giriş belgelerini tek bir belgede birleştirir ve döndürür[`Document`](../../../aspose.words/document/) son belgenin örneği.

```csharp
public static Document Merge(Document[] inputDocuments, MergeFormatMode mergeFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputDocuments | Document[] | Giriş belgeleri. |
| mergeFormatMode | MergeFormatMode | Çakışan biçimlendirmelerin nasıl birleştirileceğini belirtir. |

## Örnekler

Giriş belgelerinin tek bir belge örneğinde nasıl birleştirileceğini gösterir.

```csharp
DocumentBuilder firstDoc = new DocumentBuilder();
firstDoc.Font.Size = 16;
firstDoc.Font.Color = Color.Blue;
firstDoc.Write("Hello first word!");

DocumentBuilder secondDoc = new DocumentBuilder();
secondDoc.Write("Hello second word!");

Document mergedDoc = Merger.Merge(new Document[] { firstDoc.Document, secondDoc.Document }, MergeFormatMode.KeepSourceLayout);
Assert.AreEqual("Hello first word!\fHello second word!\f", mergedDoc.GetText());
```

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Merge(*Stream, Stream[], [SaveFormat](../../../aspose.words/saveformat/)*) {#merge_6}

Belirtilen giriş çıkış akışlarını ve son belge biçimini kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| outputStream | Stream | Çıktı akışı. |
| inputStreams | Stream[] | Giriş akışları. |
| saveFormat | SaveFormat | Kaydetme biçimi. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Örnekler

Akıştaki belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Akıştan belgeleri birleştirmenin birkaç yolu vardır:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Merge(*Stream, Stream[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_7}

Belirtilen giriş çıkış akışlarını ve kaydetme seçeneklerini kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| outputStream | Stream | Çıktı akışı. |
| inputStreams | Stream[] | Giriş akışları. |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |
| mergeFormatMode | MergeFormatMode | Çakışan biçimlendirmelerin nasıl birleştirileceğini belirtir. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Örnekler

Akıştaki belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Akıştan belgeleri birleştirmenin birkaç yolu vardır:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Merge(*Stream, Stream[], LoadOptions[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_5}

Belirtilen giriş çıkış akışlarını ve kaydetme seçeneklerini kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, LoadOptions[] loadOptions, 
    SaveOptions saveOptions, MergeFormatMode mergeFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| outputStream | Stream | Çıktı akışı. |
| inputStreams | Stream[] | Giriş akışları. |
| loadOptions | LoadOptions[] | Giriş dosyaları için yükleme seçenekleri. |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |
| mergeFormatMode | MergeFormatMode | Çakışan biçimlendirmelerin nasıl birleştirileceğini belirtir. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Örnekler

Akıştaki belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Akıştan belgeleri birleştirmenin birkaç yolu vardır:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### Ayrıca bakınız

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Merge(*Stream[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_2}

Verilen giriş belgelerini tek bir belgede birleştirir ve döndürür[`Document`](../../../aspose.words/document/) son belgenin örneği.

```csharp
public static Document Merge(Stream[] inputStreams, MergeFormatMode mergeFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStreams | Stream[] | Giriş akışları. |
| mergeFormatMode | MergeFormatMode | Çakışan biçimlendirmelerin nasıl birleştirileceğini belirtir. |

## Örnekler

Akıştaki belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Akıştan belgeleri birleştirmenin birkaç yolu vardır:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Merge(*Stream[], LoadOptions[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_1}

Verilen giriş belgelerini tek bir belgede birleştirir ve döndürür[`Document`](../../../aspose.words/document/) son belgenin örneği.

```csharp
public static Document Merge(Stream[] inputStreams, LoadOptions[] loadOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStreams | Stream[] | Giriş akışları. |
| loadOptions | LoadOptions[] | Giriş dosyaları için yükleme seçenekleri. |
| mergeFormatMode | MergeFormatMode | Çakışan biçimlendirmelerin nasıl birleştirileceğini belirtir. |

## Örnekler

Akıştaki belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Akıştan belgeleri birleştirmenin birkaç yolu vardır:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

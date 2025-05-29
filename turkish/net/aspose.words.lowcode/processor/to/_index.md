---
title: Processor.To
linktitle: To
articleTitle: To
second_title: .NET için Aspose.Words
description: Çıktı dosyalarını net bir şekilde tanımlayan, verimliliği artıran ve veri yönetimi görevlerinizi kolaylaştıran işlemci yöntemimizle iş akışınızı optimize edin.
type: docs
weight: 30
url: /tr/net/aspose.words.lowcode/processor/to/
---
## To(*string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_5}

İşlemci için çıktı dosyasını belirtir.

```csharp
public Processor To(string output, SaveOptions saveOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| output | String | Çıktı dosya adı. |
| saveOptions | SaveOptions | İsteğe bağlı kaydetme seçenekleri. Belirtilmezse, kaydetme biçimi dosya uzantısı tarafından belirlenir. |

### Geri dönüş değeri

Belirtilen çıktı dosyasıyla işlemciyi döndürür.

## Notlar

Çıktı birden fazla dosyadan oluşuyorsa, belirtilen çıktı dosya adı, her parça için 'outputFile_partIndex.extension' kuralını izleyerek dosya adı 'yi oluşturmak için kullanılır.

## Örnekler

Bağlam kullanılarak tek satır kodla belgelerin nasıl dönüştürüleceğini gösterir.

```csharp
string doc = MyDir + "Big document.docx";

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.1.pdf")
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.2.pdf", SaveFormat.Rtf)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Create(new ConverterContext())
    .From(doc, loadOptions)
    .To(ArtifactsDir + "LowCode.ConvertContext.3.docx", saveOptions)
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.Png))
    .Execute();
```

Bağlam kullanılarak belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Belgeleri birleştirmenin birkaç yolu vardır:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.1.docx")
    .Execute();

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1, firstLoadOptions)
    .From(inputDoc2, secondLoadOptions)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.2.docx", SaveFormat.Docx)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.3.docx", saveOptions)
    .Execute();
```

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## To(*string, [SaveFormat](../../../aspose.words/saveformat/)*) {#to_4}

İşlemci için çıktı dosyasını belirtir.

```csharp
public Processor To(string output, SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| output | String | Çıktı dosya adı. |
| saveFormat | SaveFormat | Kaydetme biçimi. Belirtilmezse, kaydetme biçimi dosya uzantısı tarafından belirlenir. |

### Geri dönüş değeri

Belirtilen çıktı dosyasıyla işlemciyi döndürür.

## Notlar

Çıktı birden fazla dosyadan oluşuyorsa, belirtilen çıktı dosya adı, her parça için 'outputFile_partIndex.extension' kuralını izleyerek dosya adı 'yi oluşturmak için kullanılır.

## Örnekler

Bağlam kullanılarak belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Belgeleri birleştirmenin birkaç yolu vardır:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.1.docx")
    .Execute();

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1, firstLoadOptions)
    .From(inputDoc2, secondLoadOptions)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.2.docx", SaveFormat.Docx)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.3.docx", saveOptions)
    .Execute();
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## To(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_3}

İşlemci için çıkış akışını belirtir.

```csharp
public Processor To(Stream output, SaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| output | Stream | Çıkış akışı. |
| saveOptions | SaveOptions | Seçenekleri kaydet. |

### Geri dönüş değeri

Belirtilen çıktı akışına sahip işlemciyi döndürür.

## Notlar

Çıktı birden fazla dosyadan oluşuyorsa, yalnızca ilk kısım belirtilen akışa kaydedilecektir.

## Örnekler

Bağlam kullanılarak tek satır kodla bir akıştan belgelerin nasıl dönüştürüleceğini gösterir.

```csharp
string doc = MyDir + "Document.docx";
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn)
            .To(streamOut, SaveFormat.Rtf)
            .Execute();

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn, loadOptions)
            .To(streamOut, saveOptions)
            .Execute();

    List<Stream> pages = new List<Stream>();
    Converter.Create(new ConverterContext())
        .From(doc)
        .To(pages, new ImageSaveOptions(SaveFormat.Png))
        .Execute();
}
```

Bağlam kullanılarak akıştaki belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Belgeleri birleştirmenin birkaç yolu vardır:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn)
            .From(secondStreamIn)
            .To(streamOut, saveOptions)
            .Execute();

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn, firstLoadOptions)
            .From(secondStreamIn, secondLoadOptions)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
    }
}
```

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## To(*Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#to_2}

İşlemci için çıkış akışını belirtir.

```csharp
public Processor To(Stream output, SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| output | Stream | Çıkış akışı. |
| saveFormat | SaveFormat | Biçimi kaydet. |

### Geri dönüş değeri

Belirtilen çıktı akışına sahip işlemciyi döndürür.

## Notlar

Çıktı birden fazla dosyadan oluşuyorsa, yalnızca ilk kısım belirtilen akışa kaydedilecektir.

## Örnekler

Bağlam kullanılarak tek satır kodla bir akıştan belgelerin nasıl dönüştürüleceğini gösterir.

```csharp
string doc = MyDir + "Document.docx";
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn)
            .To(streamOut, SaveFormat.Rtf)
            .Execute();

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn, loadOptions)
            .To(streamOut, saveOptions)
            .Execute();

    List<Stream> pages = new List<Stream>();
    Converter.Create(new ConverterContext())
        .From(doc)
        .To(pages, new ImageSaveOptions(SaveFormat.Png))
        .Execute();
}
```

Bağlam kullanılarak akıştaki belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Belgeleri birleştirmenin birkaç yolu vardır:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn)
            .From(secondStreamIn)
            .To(streamOut, saveOptions)
            .Execute();

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn, firstLoadOptions)
            .From(secondStreamIn, secondLoadOptions)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
    }
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## To(*List&lt;Stream&gt;, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_1}

Çıktı Belge akışları listesini belirtir.

```csharp
public Processor To(List<Stream> output, SaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| output | List`1 | Çıktı belge akışları listesi. |
| saveOptions | SaveOptions | Seçenekleri kaydet. |

### Geri dönüş değeri

Belirtilen çıktı belge akışları listesiyle işlemciyi döndürür.

## Notlar

Çıktı birden fazla dosyadan oluşuyorsa (örneğin resimler veya bölünmüş belge parçaları), her parça için bir akış belirtilen listeye eklenir. Çıktı tek bir dosyaysa, listeye yalnızca bir akış eklenir. Oluşturulan akışların imha edilmesi son kullanıcının sorumluluğundadır.

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## To(*List&lt;Stream&gt;, [SaveFormat](../../../aspose.words/saveformat/)*) {#to}

Çıktı Belge akışları listesini belirtir.

```csharp
public Processor To(List<Stream> output, SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| output | List`1 | Çıktı belge akışları listesi. |
| saveFormat | SaveFormat | Biçimi kaydet. |

### Geri dönüş değeri

Belirtilen çıktı belge akışları listesiyle işlemciyi döndürür.

## Notlar

Çıktı birden fazla dosyadan oluşuyorsa (örneğin resimler veya bölünmüş belge parçaları), her parça için bir akış belirtilen listeye eklenir. Çıktı tek bir dosyaysa, listeye yalnızca bir akış eklenir. Oluşturulan akışların imha edilmesi son kullanıcının sorumluluğundadır.

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

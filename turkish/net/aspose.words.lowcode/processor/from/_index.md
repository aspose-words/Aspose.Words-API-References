---
title: Processor.From
linktitle: From
articleTitle: From
second_title: .NET için Aspose.Words
description: Giriş belgelerini etkin bir şekilde işleyen, kusursuz işleme ve gelişmiş üretkenlik sağlayan işlemcimizle iş akışınızı geliştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.lowcode/processor/from/
---
## From(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#from_1}

İşleme için giriş belgesini belirtir.

```csharp
public Processor From(string input, LoadOptions loadOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| input | String | Giriş belgesi dosya adı. |
| loadOptions | LoadOptions | Belgeyi yüklemek için kullanılan isteğe bağlı yükleme seçenekleri. |

### Geri dönüş değeri

Belirtilen giriş dosyasıyla işlemciyi döndürür.

## Notlar

İşlemci yalnızca bir dosyayı girdi olarak kabul ederse, yalnızca son belirtilen dosya işlenecektir. [`Merger`](../../merger/) işlemci birden fazla dosyayı girdi olarak kabul eder, sonuç olarak belirtilen tüm belgeler birleştirilir. [`Converter`](../../converter/) işlemci yalnızca bir dosyayı girdi olarak kabul eder, bu nedenle yalnızca son belirtilen dosya dönüştürülecektir.

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

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Processor](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## From(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#from}

İşleme için giriş belgesini belirtir.

```csharp
public Processor From(Stream input, LoadOptions loadOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| input | Stream | Giriş belge akışı. |
| loadOptions | LoadOptions | Belgeyi yüklemek için kullanılan isteğe bağlı yükleme seçenekleri. |

### Geri dönüş değeri

Belirtilen giriş dosya akışına sahip işlemciyi döndürür.

## Notlar

İşlemci yalnızca bir dosyayı girdi olarak kabul ederse, yalnızca son belirtilen dosya işlenecektir. [`Merger`](../../merger/) işlemci birden fazla dosyayı girdi olarak kabul eder, sonuç olarak belirtilen tüm belgeler birleştirilir. [`Converter`](../../converter/) işlemci yalnızca bir dosyayı girdi olarak kabul eder, bu nedenle yalnızca son belirtilen dosya dönüştürülecektir.

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

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Processor](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

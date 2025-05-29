---
title: Converter.Create
linktitle: Create
articleTitle: Create
second_title: .NET için Aspose.Words
description: Kusursuz veri dönüşümü için güçlü Dönüştürücü Oluşturma yöntemimizle dönüştürücü işlemcinin yeni bir örneğini zahmetsizce oluşturun.
type: docs
weight: 10
url: /tr/net/aspose.words.lowcode/converter/create/
---
## Create() {#create}

Dönüştürücü işlemcinin yeni bir örneğini oluşturur.

```csharp
public static Converter Create()
```

### Ayrıca bakınız

* class [Converter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Create(*[ConverterContext](../../convertercontext/)*) {#create_1}

Dönüştürücü işlemcinin yeni bir örneğini oluşturur.

```csharp
public static Converter Create(ConverterContext context)
```

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

### Ayrıca bakınız

* class [ConverterContext](../../convertercontext/)
* class [Converter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

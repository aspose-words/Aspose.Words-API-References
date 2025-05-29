---
title: SplitterContext Class
linktitle: SplitterContext
articleTitle: SplitterContext
second_title: .NET için Aspose.Words
description: Verimli belge bölme için Aspose.Words.LowCode.SplitterContext sınıfını keşfedin, kusursuz entegrasyon ve güçlü işlevsellikle iş akışınızı geliştirin.
type: docs
weight: 4430
url: /tr/net/aspose.words.lowcode/splittercontext/
---
## SplitterContext class

Belge ayırıcı bağlamı.

```csharp
public class SplitterContext : ProcessorContext
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [SplitterContext](splittercontext/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | İşlemci tarafından kullanılan yazı tipi ayarları. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | İşlemci tarafından kullanılan belge düzeni seçenekleri. |
| [SplitOptions](../../aspose.words.lowcode/splittercontext/splitoptions/) { get; } | Belge bölme seçenekleri. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | İşlemci tarafından kullanılan uyarı geri araması. |

## Örnekler

Belgenin bağlam kullanılarak sayfalara nasıl bölüneceğini gösterir.

```csharp
string doc = MyDir + "Big document.docx";

SplitterContext splitterContext = new SplitterContext();
splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

Splitter.Create(splitterContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.SplitContextDocument.docx")
    .Execute();
```

Bağlamı kullanarak belgenin akıştan sayfalara göre nasıl bölüneceğini gösterir.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    SplitterContext splitterContext = new SplitterContext();
    splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

    List<Stream> pages = new List<Stream>();
    Splitter.Create(splitterContext)
        .From(streamIn)
        .To(pages, SaveFormat.Docx)
        .Execute();
}
```

### Ayrıca bakınız

* class [ProcessorContext](../processorcontext/)
* ad alanı [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../)

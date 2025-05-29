---
title: SplitterContext.SplitOptions
linktitle: SplitOptions
articleTitle: SplitOptions
second_title: .NET için Aspose.Words
description: Verimli ve esnek içerik bölme için SplitterContext'in SplitOptions özelliğiyle belge yönetimini nasıl optimize edeceğinizi keşfedin. İş akışınızı bugün geliştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.lowcode/splittercontext/splitoptions/
---
## SplitterContext.SplitOptions property

Belge bölme seçenekleri.

```csharp
public SplitOptions SplitOptions { get; }
```

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

* class [SplitOptions](../../splitoptions/)
* class [SplitterContext](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

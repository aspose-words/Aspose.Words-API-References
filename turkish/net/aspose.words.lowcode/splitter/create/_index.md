---
title: Splitter.Create
linktitle: Create
articleTitle: Create
second_title: .NET için Aspose.Words
description: Kusursuz entegrasyon ve gelişmiş performans için kolay takip edilebilir kılavuzumuzla ayırıcı işlemcinin yeni bir örneğini nasıl verimli bir şekilde oluşturacağınızı keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.lowcode/splitter/create/
---
## Splitter.Create method

Ayırıcı işlemcinin yeni bir örneğini oluşturur.

```csharp
public static Splitter Create(SplitterContext context)
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

* class [SplitterContext](../../splittercontext/)
* class [Splitter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

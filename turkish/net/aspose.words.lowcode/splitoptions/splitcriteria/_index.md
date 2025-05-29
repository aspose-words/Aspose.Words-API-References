---
title: SplitOptions.SplitCriteria
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: .NET için Aspose.Words
description: SplitOptions SplitCriteria özelliğinin, içeriğinizi yönetilebilir bölümlere verimli bir şekilde bölerek belge yönetimini nasıl geliştirdiğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.lowcode/splitoptions/splitcriteria/
---
## SplitOptions.SplitCriteria property

Belgeyi parçalara ayırma ölçütlerini belirtir.

```csharp
public SplitCriteria SplitCriteria { get; set; }
```

## Örnekler

Belgenin sayfalara göre nasıl bölüneceğini gösterir.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Ayrıca bakınız

* enum [SplitCriteria](../../splitcriteria/)
* class [SplitOptions](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

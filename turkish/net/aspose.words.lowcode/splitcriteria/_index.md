---
title: SplitCriteria Enum
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: .NET için Aspose.Words
description: Verimli belge bölme için Aspose.Words.LowCode.SplitCriteria enum'unu keşfedin. Sorunsuz parça yönetimi için çok yönlü seçeneklerle iş akışınızı optimize edin.
type: docs
weight: 4400
url: /tr/net/aspose.words.lowcode/splitcriteria/
---
## SplitCriteria enumeration

Belgenin parçalara nasıl bölüneceğini belirtir.

```csharp
public enum SplitCriteria
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Page | `0` | Belgenin sayfalara bölündüğünü belirtir. |
| SectionBreak | `1` | Belgenin herhangi bir türdeki bölüm sonuyla parçalara bölüneceğini belirtir. |
| Style | `2` | Belgenin, belirtilen stil kullanılarak biçimlendirilmiş bir paragrafta parçalara bölüneceğini belirtir.[`SplitStyle`](../splitoptions/splitstyle/) . |

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

* ad alanı [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../)

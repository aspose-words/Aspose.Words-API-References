---
title: Style.SemiHidden
linktitle: SemiHidden
articleTitle: SemiHidden
second_title: .NET için Aspose.Words
description: SemiHidden özelliğinin Stil galerisinde ve görev bölmesinde stil görünürlüğünü nasıl kontrol ettiğini, tasarım iş akışınızı ve verimliliğinizi nasıl artırdığını keşfedin.
type: docs
weight: 170
url: /tr/net/aspose.words/style/semihidden/
---
## Style.SemiHidden property

Stilin Stiller galerisinden ve Stiller görev bölmesinden gizlenip gizlenmeyeceğini alır/ayarlar.

```csharp
public bool SemiHidden { get; set; }
```

## Örnekler

Bir stilin nasıl önceliklendirileceğini ve gizleneceğini gösterir.

```csharp
Document doc = new Document();
Style styleTitle = doc.Styles[StyleIdentifier.Subtitle];

if (styleTitle.Priority == 9)
    styleTitle.Priority = 10;

if (!styleTitle.UnhideWhenUsed)
    styleTitle.UnhideWhenUsed = true;

if (styleTitle.SemiHidden)
    styleTitle.SemiHidden = true;

doc.Save(ArtifactsDir + "Styles.StylePriority.docx");
```

### Ayrıca bakınız

* class [Style](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

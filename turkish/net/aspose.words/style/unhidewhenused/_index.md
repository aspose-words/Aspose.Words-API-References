---
title: Style.UnhideWhenUsed
linktitle: UnhideWhenUsed
articleTitle: UnhideWhenUsed
second_title: .NET için Aspose.Words
description: Stiller için UnhideWhenUsed özelliğinin nasıl yönetileceğini keşfedin. Belgenizin tasarımını geliştirmek için Stiller galerisinde ve görev bölmesinde görünürlüğü kontrol edin.
type: docs
weight: 210
url: /tr/net/aspose.words/style/unhidewhenused/
---
## Style.UnhideWhenUsed property

Geçerli belgede kullanılan stilin Stiller galerisinden ve Stiller görev bölmesinden gizlenip gizlenmeyeceğini alır/ayarlar. Kullanılan stilin Stiller galerisinde gösterilmesi gerektiğinde doğrudur.

```csharp
public bool UnhideWhenUsed { get; set; }
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

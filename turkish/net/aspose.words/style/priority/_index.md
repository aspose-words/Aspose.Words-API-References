---
title: Style.Priority
linktitle: Priority
articleTitle: Priority
second_title: .NET için Aspose.Words
description: Görev bölmenizde stil sıralamasını optimize etmek için Stil Önceliği ayarlarını nasıl yöneteceğinizi keşfedin. Verimli stil organizasyonuyla iş akışınızı geliştirin!
type: docs
weight: 160
url: /tr/net/aspose.words/style/priority/
---
## Style.Priority property

Stiller görev bölmesinde stilleri sıralama önceliğini temsil eden tamsayı değerini alır/ayarlar.

```csharp
public int Priority { get; set; }
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

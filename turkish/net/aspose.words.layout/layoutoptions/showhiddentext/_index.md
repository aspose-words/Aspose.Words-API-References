---
title: LayoutOptions.ShowHiddenText
linktitle: ShowHiddenText
articleTitle: ShowHiddenText
second_title: .NET için Aspose.Words
description: LayoutOptions ShowHiddenText özelliğini keşfedin, belgelerinizdeki gizli metinlerin işlenmesini kolayca kontrol edin. İçerik görünürlüğünüzü bugün optimize edin!
type: docs
weight: 80
url: /tr/net/aspose.words.layout/layoutoptions/showhiddentext/
---
## LayoutOptions.ShowHiddenText property

Belgedeki gizli metnin işlenip işlenmediğine ilişkin göstergeyi alır veya ayarlar. Varsayılan`YANLIŞ` .

```csharp
public bool ShowHiddenText { get; set; }
```

## Notlar

Bu özellik yalnızca metni değil, tüm gizli içeriği etkiler.

## Örnekler

İşlenmiş çıktı belgesinde metnin nasıl gizleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Gizli metin ekleyin, ardından işlenmiş belgeden bunu çıkarmak isteyip istemediğimizi belirtin.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

### Ayrıca bakınız

* class [LayoutOptions](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)

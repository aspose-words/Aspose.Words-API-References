---
title: DocumentBase.PageColor
linktitle: PageColor
articleTitle: PageColor
second_title: Aspose.Words for .NET
description: DocumentBase PageColor mülk. Belgenin sayfa rengini alır veya ayarlar. Bu özellik daha basit bir versiyonudurBackgroundShape  C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words/documentbase/pagecolor/
---
## DocumentBase.PageColor property

Belgenin sayfa rengini alır veya ayarlar. Bu özellik, daha basit bir versiyonudur[`BackgroundShape`](../backgroundshape/) .

```csharp
public Color PageColor { get; set; }
```

## Notlar

Bu özellik, belge için düz sayfa rengi belirlemenin basit bir yolunu sağlar. Bu özelliğin ayarlanması, uygun bir renk oluşturur ve ayarlar.[`BackgroundShape`](../backgroundshape/).

Sayfa rengi ayarlanmamışsa (örn. belgede arka plan şekli yoksa) döndürür Empty.

## Örnekler

Bir belgenin tüm sayfaları için arka plan renginin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.PageColor = System.Drawing.Color.LightGray;

doc.Save(ArtifactsDir + "DocumentBase.SetPageColor.docx");
```

### Ayrıca bakınız

* class [DocumentBase](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

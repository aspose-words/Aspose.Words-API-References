---
title: DocumentBase.PageColor
linktitle: PageColor
articleTitle: PageColor
second_title: .NET için Aspose.Words
description: Belgenizin sayfa rengini kolayca özelleştirmek için DocumentBase PageColor özelliğini keşfedin. Bu kullanıcı dostu özellik ile tasarımı basitleştirin!
type: docs
weight: 70
url: /tr/net/aspose.words/documentbase/pagecolor/
---
## DocumentBase.PageColor property

Belgenin sayfa rengini alır veya ayarlar. Bu özellik, daha basit bir sürümüdür[`BackgroundShape`](../backgroundshape/) .

```csharp
public Color PageColor { get; set; }
```

## Notlar

Bu özellik, belge için düz bir sayfa rengi belirtmenin basit bir yolunu sağlar. Bu özelliğin ayarlanması, uygun bir renk oluşturur ve ayarlar.[`BackgroundShape`](../backgroundshape/).

Sayfa rengi ayarlanmamışsa (örneğin belgede arka plan şekli yoksa) returns Empty.

## Örnekler

Bir belgenin tüm sayfalarının arka plan renginin nasıl ayarlanacağını gösterir.

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

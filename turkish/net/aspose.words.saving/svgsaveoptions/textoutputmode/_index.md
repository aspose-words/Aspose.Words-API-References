---
title: SvgSaveOptions.TextOutputMode
second_title: Aspose.Words for .NET API Referansı
description: SvgSaveOptions mülk. Metnin SVGde nasıl oluşturulması gerektiğini belirleyen bir değer alır veya ayarlar.
type: docs
weight: 90
url: /tr/net/aspose.words.saving/svgsaveoptions/textoutputmode/
---
## SvgSaveOptions.TextOutputMode property

Metnin SVG'de nasıl oluşturulması gerektiğini belirleyen bir değer alır veya ayarlar.

```csharp
public SvgTextOutputMode TextOutputMode { get; set; }
```

### Notlar

SVG formatında kaydederken bir belge içindeki metnin nasıl render olması gerektiğine ilişkin modu almak veya ayarlamak için bu özelliği kullanın.

Varsayılan değer:UseTargetMachineFonts.

### Örnekler

Bir .docx belgesini .svg'ye dönüştürürken görüntülerin özelliklerinin nasıl taklit edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// SvgSaveOptions nesnesini, sayfa kenarlıkları veya seçilebilir metin olmadan kaydedilecek şekilde yapılandırın.
SvgSaveOptions options = new SvgSaveOptions
{
    FitToViewPort = true,
    ShowPageBorder = false,
    TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs
};

doc.Save(ArtifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### Ayrıca bakınız

* enum [SvgTextOutputMode](../../svgtextoutputmode/)
* class [SvgSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../svgsaveoptions/)
* toplantı [Aspose.Words](../../../)



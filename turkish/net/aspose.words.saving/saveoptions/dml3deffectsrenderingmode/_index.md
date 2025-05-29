---
title: SaveOptions.Dml3DEffectsRenderingMode
linktitle: Dml3DEffectsRenderingMode
articleTitle: Dml3DEffectsRenderingMode
second_title: .NET için Aspose.Words
description: Uygulamalarınızda gelişmiş görsel kalite için 3B efekt oluşturmayı kolayca kontrol etmek amacıyla SaveOptions Dml3DEffectsRenderingMode özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/saveoptions/dml3deffectsrenderingmode/
---
## SaveOptions.Dml3DEffectsRenderingMode property

3B efektlerin nasıl işleneceğini belirleyen bir değer alır veya ayarlar.

```csharp
public Dml3DEffectsRenderingMode Dml3DEffectsRenderingMode { get; set; }
```

## Notlar

Varsayılan değer:Basic .

## Örnekler

3D efektlerin nasıl oluşturulduğunu gösterir.

```csharp
Document doc = new Document(MyDir + "DrawingML shape 3D effects.docx");

RenderCallback warningCallback = new RenderCallback();
doc.WarningCallback = warningCallback;

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.Dml3DEffectsRenderingMode = Dml3DEffectsRenderingMode.Advanced;

doc.Save(ArtifactsDir + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
```

### Ayrıca bakınız

* enum [Dml3DEffectsRenderingMode](../../dml3deffectsrenderingmode/)
* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)

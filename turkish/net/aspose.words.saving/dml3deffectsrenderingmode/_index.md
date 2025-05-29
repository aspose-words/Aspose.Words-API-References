---
title: Dml3DEffectsRenderingMode Enum
linktitle: Dml3DEffectsRenderingMode
articleTitle: Dml3DEffectsRenderingMode
second_title: .NET için Aspose.Words
description: Üstün 3B şekil oluşturma ve görsel etki için Aspose.Words'ün Dml3DEffectsRenderingMode enum'unu kullanarak belgelerinizi nasıl geliştirebileceğinizi keşfedin.
type: docs
weight: 5650
url: /tr/net/aspose.words.saving/dml3deffectsrenderingmode/
---
## Dml3DEffectsRenderingMode enumeration

3B şekil efektlerinin nasıl işleneceğini belirtir.

```csharp
public enum Dml3DEffectsRenderingMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Basic | `0` | Dahili motora dayalı hafif ve kararlı bir işleme, ancak aydınlatma, malzemeler ve diğer ek efektler gibi gelişmiş efektler bu mod kullanıldığında görüntülenmez. Ayrıntılar için lütfen belgelere bakın. |
| Advanced | `1` | Eğimler, aydınlatma ve malzemeler gibi gelişmiş 3B efektler de dahil olmak üzere özel efektlerin genişletilmiş bir listesinin işlenmesi. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)

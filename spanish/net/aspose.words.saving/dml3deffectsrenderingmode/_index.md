---
title: Dml3DEffectsRenderingMode Enum
linktitle: Dml3DEffectsRenderingMode
articleTitle: Dml3DEffectsRenderingMode
second_title: Aspose.Words para .NET
description: Descubra cómo mejorar sus documentos con la enumeración Dml3DEffectsRenderingMode de Aspose.Words para lograr una representación de formas 3D superior y un mayor impacto visual.
type: docs
weight: 5650
url: /es/net/aspose.words.saving/dml3deffectsrenderingmode/
---
## Dml3DEffectsRenderingMode enumeration

Especifica cómo se representan los efectos de forma 3D.

```csharp
public enum Dml3DEffectsRenderingMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Basic | `0` | Una representación liviana y estable, basada en el motor interno, pero los efectos avanzados como iluminación, materiales y otros efectos adicionales no se muestran cuando se usa este modo. Consulte la documentación para obtener más detalles. |
| Advanced | `1` | Representación de una lista ampliada de efectos especiales, incluidos efectos 3D avanzados, como biseles, iluminación y materiales. |

## Ejemplos

Muestra cómo se representan los efectos 3D.

```csharp
Document doc = new Document(MyDir + "DrawingML shape 3D effects.docx");

RenderCallback warningCallback = new RenderCallback();
doc.WarningCallback = warningCallback;

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.Dml3DEffectsRenderingMode = Dml3DEffectsRenderingMode.Advanced;

doc.Save(ArtifactsDir + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)

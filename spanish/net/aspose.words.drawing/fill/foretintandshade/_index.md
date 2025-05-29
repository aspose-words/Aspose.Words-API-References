---
title: Fill.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words para .NET
description: Ajuste la propiedad ForeTintAndShade para aclarar u oscurecer fácilmente su color de primer plano, mejorando su diseño con precisión y creatividad.
type: docs
weight: 90
url: /es/net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

Obtiene o establece un valor doble que aclara u oscurece el color de primer plano.

```csharp
public double ForeTintAndShade { get; set; }
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentOutOfRangeException | Se lanza si se establece esta propiedad en un valor menor que -1 o mayor que 1. |

## Observaciones

Los valores permitidos están en el rango de -1 (el más oscuro) a 1 (el más claro) para esta propiedad.

Cero (0) es neutral.

## Ejemplos

Muestra cómo administrar el aclarado y el oscurecimiento del color de fuente del primer plano.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

Fill textFill = doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Fill;
textFill.ForeThemeColor = ThemeColor.Accent1;
if (textFill.ForeTintAndShade == 0)
    textFill.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.FillTintAndShade.docx");
```

### Ver también

* class [Fill](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)

---
title: Fill.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words para .NET
description: Fill ForeTintAndShade propiedad. Obtiene o establece un valor doble que aclara u oscurece el color de primer plano en C#.
type: docs
weight: 80
url: /es/net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

Obtiene o establece un valor doble que aclara u oscurece el color de primer plano.

```csharp
public double ForeTintAndShade { get; set; }
```

## Observaciones

Los valores permitidos están dentro del rango de -1 (el más oscuro) a 1 (el más claro) para esta propiedad. Cero (0) es neutral. Intentar establecer esta propiedad en un valor inferior a -1 o superior a 1 da como resultadoArgumentOutOfRangeException.

## Ejemplos

Muestra cómo gestionar el color de fuente de primer plano que se aclara y oscurece.

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

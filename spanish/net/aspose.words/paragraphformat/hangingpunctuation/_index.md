---
title: ParagraphFormat.HangingPunctuation
linktitle: HangingPunctuation
articleTitle: HangingPunctuation
second_title: Aspose.Words para .NET
description: Descubre cómo mejorar el diseño de tu texto con la propiedad Puntuación Saliente en ParagraphFormat. ¡Optimiza la legibilidad y el estilo sin esfuerzo!
type: docs
weight: 130
url: /es/net/aspose.words/paragraphformat/hangingpunctuation/
---
## ParagraphFormat.HangingPunctuation property

Obtiene o establece un indicador que indica si la puntuación colgante está habilitada para el párrafo actual.

```csharp
public bool HangingPunctuation { get; set; }
```

## Ejemplos

Muestra cómo establecer propiedades especiales para la tipografía asiática.

```csharp
Document doc = new Document(MyDir + "Document.docx");

ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.FarEastLineBreakControl = true;
format.WordWrap = false;
format.HangingPunctuation = true;

doc.Save(ArtifactsDir + "ParagraphFormat.AsianTypographyProperties.docx");
```

### Ver también

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

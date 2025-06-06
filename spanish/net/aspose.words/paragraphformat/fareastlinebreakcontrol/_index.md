---
title: ParagraphFormat.FarEastLineBreakControl
linktitle: FarEastLineBreakControl
articleTitle: FarEastLineBreakControl
second_title: Aspose.Words para .NET
description: Descubra la propiedad ParagraphFormat FarEastLineBreakControl, que habilita reglas de salto de línea del este de Asia para un formato de texto preciso en sus documentos.
type: docs
weight: 110
url: /es/net/aspose.words/paragraphformat/fareastlinebreakcontrol/
---
## ParagraphFormat.FarEastLineBreakControl property

Obtiene o establece un indicador que indica si se aplican las reglas de salto de línea del este de Asia al párrafo actual.

```csharp
public bool FarEastLineBreakControl { get; set; }
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

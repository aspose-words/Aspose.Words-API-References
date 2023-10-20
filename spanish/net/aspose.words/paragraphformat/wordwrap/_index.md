---
title: ParagraphFormat.WordWrap
linktitle: WordWrap
articleTitle: WordWrap
second_title: Aspose.Words para .NET
description: ParagraphFormat WordWrap propiedad. Si esta propiedad esFALSO  El texto latino en medio de una palabra se puede ajustar para el párrafo actual. De lo contrario el texto en latín se envuelve con palabras completas en C#.
type: docs
weight: 410
url: /es/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

Si esta propiedad es`FALSO` , El texto latino en medio de una palabra se puede ajustar para el párrafo actual. De lo contrario, el texto en latín se envuelve con palabras completas.

```csharp
public bool WordWrap { get; set; }
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

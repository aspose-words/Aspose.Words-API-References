---
title: ParagraphFormat.WordWrap
linktitle: WordWrap
articleTitle: WordWrap
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad ParagraphFormat WordWrap afecta el ajuste de texto en Word. Aprenda a controlar el flujo de texto en latín para mejorar la legibilidad de los documentos.
type: docs
weight: 420
url: /es/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

Si esta propiedad es`FALSO` El texto en latín en medio de una palabra se puede ajustar durante el párrafo actual. De lo contrario, se ajusta con palabras completas.

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

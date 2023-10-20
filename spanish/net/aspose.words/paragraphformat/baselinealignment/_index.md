---
title: ParagraphFormat.BaselineAlignment
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words para .NET
description: ParagraphFormat BaselineAlignment propiedad. Obtiene o establece la posición vertical de las fuentes en una línea en C#.
type: docs
weight: 40
url: /es/net/aspose.words/paragraphformat/baselinealignment/
---
## ParagraphFormat.BaselineAlignment property

Obtiene o establece la posición vertical de las fuentes en una línea.

```csharp
public BaselineAlignment BaselineAlignment { get; set; }
```

## Ejemplos

Muestra cómo configurar la posición vertical de las fuentes en una línea.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;
if (format.BaselineAlignment == BaselineAlignment.Auto)
{                
    format.BaselineAlignment = BaselineAlignment.Top;
}

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphBaselineAlignment.docx");
```

### Ver también

* enum [BaselineAlignment](../../baselinealignment/)
* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

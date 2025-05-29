---
title: Font.Subscript
linktitle: Subscript
articleTitle: Subscript
second_title: Aspose.Words para .NET
description: Descubre la propiedad Subíndice de fuente. Formatea fácilmente el texto como subíndice para mejorar la legibilidad y el estilo de tus documentos. ¡Mejora tu diseño hoy mismo!
type: docs
weight: 440
url: /es/net/aspose.words/font/subscript/
---
## Font.Subscript property

Verdadero si la fuente está formateada como subíndice.

```csharp
public bool Subscript { get; set; }
```

## Ejemplos

Muestra cómo formatear el texto para desplazar su posición.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

//Eleva esta secuencia de texto 5 puntos por encima de la línea base.
Run run = new Run(doc, "Raised text. ");
run.Font.Position = 5;
para.AppendChild(run);

// Baje esta secuencia de texto 10 puntos por debajo de la línea base.
run = new Run(doc, "Lowered text. ");
run.Font.Position = -10;
para.AppendChild(run);

//Agrega una serie de texto normal.
run = new Run(doc, "Text in its default position. ");
para.AppendChild(run);

// Agrega una serie de texto que aparece como subíndice.
run = new Run(doc, "Subscript. ");
run.Font.Subscript = true;
para.AppendChild(run);

// Agrega una serie de texto que aparece como superíndice.
run = new Run(doc, "Superscript.");
run.Font.Superscript = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.PositionSubscript.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

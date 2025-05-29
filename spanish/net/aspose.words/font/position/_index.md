---
title: Font.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words para .NET
description: Descubre la propiedad Posición de fuente y ajusta fácilmente la alineación del texto en puntos para un control preciso de tu tipografía. ¡Mejora tu diseño con posicionamiento flexible!
type: docs
weight: 310
url: /es/net/aspose.words/font/position/
---
## Font.Position property

Obtiene o establece la posición del texto (en puntos) con respecto a la línea base. Un número positivo eleva el texto y un número negativo lo baja.

```csharp
public double Position { get; set; }
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

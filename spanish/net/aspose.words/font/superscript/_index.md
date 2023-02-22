---
title: Font.Superscript
second_title: Referencia de API de Aspose.Words para .NET
description: Font propiedad. Verdadero si la fuente está formateada como superíndice.
type: docs
weight: 440
url: /es/net/aspose.words/font/superscript/
---
## Font.Superscript property

Verdadero si la fuente está formateada como superíndice.

```csharp
public bool Superscript { get; set; }
```

### Ejemplos

Muestra cómo dar formato al texto para desplazar su posición.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph) doc.GetChild(NodeType.Paragraph, 0, true);

// Eleve esta ejecución de texto 5 puntos por encima de la línea de base.
Run run = new Run(doc, "Raised text. ");
run.Font.Position = 5;
para.AppendChild(run);

// Baje esta ejecución de texto 10 puntos por debajo de la línea de base.
run = new Run(doc, "Lowered text. ");
run.Font.Position = -10;
para.AppendChild(run);

// Agrega una serie de texto normal.
run = new Run(doc, "Text in its default position. ");
para.AppendChild(run);

// Agrega una secuencia de texto que aparece como subíndice.
run = new Run(doc, "Subscript. ");
run.Font.Subscript = true;
para.AppendChild(run);

// Agrega una secuencia de texto que aparece como superíndice.
run = new Run(doc, "Superscript.");
run.Font.Superscript = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.PositionSubscript.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../font/)
* asamblea [Aspose.Words](../../../)



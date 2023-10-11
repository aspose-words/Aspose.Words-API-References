---
title: Border.LineStyle
second_title: Referencia de API de Aspose.Words para .NET
description: Border propiedad. Obtiene o establece el estilo del borde.
type: docs
weight: 40
url: /es/net/aspose.words/border/linestyle/
---
## Border.LineStyle property

Obtiene o establece el estilo del borde.

```csharp
public LineStyle LineStyle { get; set; }
```

### Observaciones

Si establece el estilo de línea en ninguno, el ancho de línea cambia automáticamente a cero.

### Ejemplos

Muestra cómo insertar una cadena rodeada por un borde en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### Ver también

* enum [LineStyle](../../linestyle/)
* class [Border](../)
* espacio de nombres [Aspose.Words](../../border/)
* asamblea [Aspose.Words](../../../)



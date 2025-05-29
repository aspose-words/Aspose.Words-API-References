---
title: Border.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words para .NET
description: Ajuste la propiedad Border LineWidth para personalizar el grosor del borde en puntos, mejorando la precisión y el atractivo visual de su diseño.
type: docs
weight: 50
url: /es/net/aspose.words/border/linewidth/
---
## Border.LineWidth property

Obtiene o establece el ancho del borde en puntos.

```csharp
public double LineWidth { get; set; }
```

## Observaciones

Si establece un ancho de línea mayor que cero cuando el estilo de línea es ninguno, el estilo de línea cambiará automáticamente a línea única.

## Ejemplos

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

* class [Border](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

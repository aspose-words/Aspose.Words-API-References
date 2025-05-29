---
title: ParagraphFormat.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words para .NET
description: Ajuste fácilmente el interlineado de sus párrafos con la propiedad ParagraphFormat LineSpacing. ¡Mejore la legibilidad y el estilo de sus documentos!
type: docs
weight: 190
url: /es/net/aspose.words/paragraphformat/linespacing/
---
## ParagraphFormat.LineSpacing property

Obtiene o establece el espacio entre líneas (en puntos) para el párrafo.

```csharp
public double LineSpacing { get; set; }
```

## Observaciones

Cuando[`LineSpacingRule`](../linespacingrule/) La propiedad está establecida enAtLeast , el espacio entre líneas puede ser mayor o igual a, pero nunca menor que el especificado`LineSpacing` valor.

Cuando[`LineSpacingRule`](../linespacingrule/) La propiedad está establecida enExactly , el espacio entre líneas nunca cambia de el especificado`LineSpacing` valor, incluso si se utiliza una fuente más grande dentro del párrafo.

## Ejemplos

Muestra cómo trabajar con el espaciado entre líneas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación se muestran tres reglas de espaciado de línea que podemos definir usando el
// Propiedad "LineSpacingRule" del párrafo para configurar el espaciado entre párrafos.
// 1 - Establezca una cantidad mínima de espaciado.
// Esto dará relleno vertical a las líneas de texto de cualquier tamaño.
// que es demasiado pequeño para mantener la altura de línea mínima.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.AtLeast;
builder.ParagraphFormat.LineSpacing = 20;

builder.Writeln("Minimum line spacing of 20.");
builder.Writeln("Minimum line spacing of 20.");

// 2 - Establecer el espaciado exacto.
// El uso de tamaños de fuente demasiado grandes para el espaciado truncará el texto.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Exactly;
builder.ParagraphFormat.LineSpacing = 5;

builder.Writeln("Line spacing of exactly 5.");
builder.Writeln("Line spacing of exactly 5.");

// 3 - Establezca el espaciado como un múltiplo del espaciado de línea predeterminado, que es 12 puntos por defecto.
// Este tipo de espaciado se adaptará a diferentes tamaños de fuente.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Multiple;
builder.ParagraphFormat.LineSpacing = 18;

builder.Writeln("Line spacing of 1.5 default lines.");
builder.Writeln("Line spacing of 1.5 default lines.");

doc.Save(ArtifactsDir + "ParagraphFormat.LineSpacing.docx");
```

### Ver también

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

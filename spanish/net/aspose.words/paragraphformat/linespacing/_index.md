---
title: ParagraphFormat.LineSpacing
second_title: Referencia de API de Aspose.Words para .NET
description: ParagraphFormat propiedad. Obtiene o establece el interlineado en puntos del párrafo.
type: docs
weight: 190
url: /es/net/aspose.words/paragraphformat/linespacing/
---
## ParagraphFormat.LineSpacing property

Obtiene o establece el interlineado (en puntos) del párrafo.

```csharp
public double LineSpacing { get; set; }
```

### Observaciones

Cuando[`LineSpacingRule`](../linespacingrule/) la propiedad está establecida enAtLeast , el interlineado puede ser mayor o igual a, pero nunca menor que el especificado`LineSpacing` valor.

Cuando[`LineSpacingRule`](../linespacingrule/) la propiedad está establecida enExactly , el interlineado nunca cambia de el especificado`LineSpacing` valor, incluso si se utiliza una fuente más grande dentro del párrafo.

### Ejemplos

Muestra cómo trabajar con el interlineado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación se muestran tres reglas de interlineado que podemos definir usando el
// propiedad "LineSpacingRule" del párrafo para configurar el espacio entre párrafos.
// 1 - Establece una cantidad mínima de espacio.
// Esto dará relleno vertical a líneas de texto de cualquier tamaño
// eso es demasiado pequeño para mantener la altura mínima de línea.
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

// 3 - Establece el espaciado como un múltiplo del espaciado entre líneas predeterminado, que es de 12 puntos por defecto.
// Este tipo de espaciado se adaptará a diferentes tamaños de fuente.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Multiple;
builder.ParagraphFormat.LineSpacing = 18;

builder.Writeln("Line spacing of 1.5 default lines.");
builder.Writeln("Line spacing of 1.5 default lines.");

doc.Save(ArtifactsDir + "ParagraphFormat.LineSpacing.docx");
```

### Ver también

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../paragraphformat/)
* asamblea [Aspose.Words](../../../)



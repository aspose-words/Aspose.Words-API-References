---
title: Font.AllCaps
second_title: Referencia de API de Aspose.Words para .NET
description: Font propiedad. Verdadero si la fuente tiene el formato de letras mayúsculas.
type: docs
weight: 10
url: /es/net/aspose.words/font/allcaps/
---
## Font.AllCaps property

Verdadero si la fuente tiene el formato de letras mayúsculas.

```csharp
public bool AllCaps { get; set; }
```

### Ejemplos

Muestra cómo formatear una ejecución para mostrar su contenido en mayúsculas.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Hay dos formas de hacer que una ejecución muestre su texto en minúsculas en mayúsculas sin cambiar el contenido.
// 1 - Establece el indicador AllCaps para mostrar todos los caracteres en mayúsculas normales:
Run run = new Run(doc, "all capitals");
run.Font.AllCaps = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

// 2 - Establece el indicador SmallCaps para mostrar todos los caracteres en minúsculas:
// Si un carácter está en minúscula, aparecerá en mayúscula
// pero tendrá la misma altura que las minúsculas (la altura x de la fuente).
// Los caracteres que originalmente estaban en mayúsculas tendrán el mismo aspecto.
run = new Run(doc, "Small Capitals");
run.Font.SmallCaps = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.Caps.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../font/)
* asamblea [Aspose.Words](../../../)



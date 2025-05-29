---
title: Font.SmallCaps
linktitle: SmallCaps
articleTitle: SmallCaps
second_title: Aspose.Words para .NET
description: Descubre la propiedad Font SmallCaps. Formatea fácilmente el texto en versalitas para mejorar la legibilidad y darle un toque elegante a tus diseños.
type: docs
weight: 370
url: /es/net/aspose.words/font/smallcaps/
---
## Font.SmallCaps property

Verdadero si la fuente está formateada en mayúsculas pequeñas.

```csharp
public bool SmallCaps { get; set; }
```

## Ejemplos

Muestra cómo formatear una ejecución para mostrar su contenido en mayúsculas.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Hay dos formas de hacer que una ejecución muestre su texto en minúsculas en mayúsculas sin cambiar el contenido.
// 1 - Establezca la bandera AllCaps para mostrar todos los caracteres en mayúsculas regulares:
Run run = new Run(doc, "all capitals");
run.Font.AllCaps = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

// 2 - Establezca la bandera SmallCaps para mostrar todos los caracteres en versalitas:
// Si un carácter está en minúscula, aparecerá en su forma mayúscula
// pero tendrá la misma altura que la minúscula (la altura x de la fuente).
//Los caracteres que originalmente estaban en mayúsculas se verán iguales.
run = new Run(doc, "Small Capitals");
run.Font.SmallCaps = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.Caps.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

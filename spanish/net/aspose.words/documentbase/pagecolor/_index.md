---
title: DocumentBase.PageColor
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentBase propiedad. Obtiene o establece el color de página del documento. Esta propiedad es una versión más simple deBackgroundShape .
type: docs
weight: 60
url: /es/net/aspose.words/documentbase/pagecolor/
---
## DocumentBase.PageColor property

Obtiene o establece el color de página del documento. Esta propiedad es una versión más simple de[`BackgroundShape`](../backgroundshape/) .

```csharp
public Color PageColor { get; set; }
```

### Observaciones

Esta propiedad proporciona una forma sencilla de especificar un color de página sólido para el documento. Al establecer esta propiedad, se crea y establece un color apropiado.[`BackgroundShape`](../backgroundshape/).

Si el color de la página no está configurado (por ejemplo, no hay una forma de fondo en el documento) devuelve Empty.

### Ejemplos

Muestra cómo establecer el color de fondo para todas las páginas de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.PageColor = System.Drawing.Color.LightGray;

doc.Save(ArtifactsDir + "DocumentBase.SetPageColor.docx");
```

### Ver también

* class [DocumentBase](../)
* espacio de nombres [Aspose.Words](../../documentbase/)
* asamblea [Aspose.Words](../../../)



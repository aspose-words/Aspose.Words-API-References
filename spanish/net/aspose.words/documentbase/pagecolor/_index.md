---
title: DocumentBase.PageColor
linktitle: PageColor
articleTitle: PageColor
second_title: Aspose.Words para .NET
description: Descubre la propiedad DocumentBase PageColor para personalizar fácilmente el color de página de tu documento. ¡Simplifica el diseño con esta función intuitiva!
type: docs
weight: 70
url: /es/net/aspose.words/documentbase/pagecolor/
---
## DocumentBase.PageColor property

Obtiene o establece el color de página del documento. Esta propiedad es una versión más simple de[`BackgroundShape`](../backgroundshape/) .

```csharp
public Color PageColor { get; set; }
```

## Observaciones

Esta propiedad proporciona una manera sencilla de especificar un color de página sólido para el documento. Al configurar esta propiedad se crea y establece un color de página sólido adecuado.[`BackgroundShape`](../backgroundshape/).

Si el color de la página no está configurado (por ejemplo, no hay forma de fondo en el documento) devuelve Empty.

## Ejemplos

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
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

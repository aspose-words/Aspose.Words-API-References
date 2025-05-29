---
title: DocumentBase.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words para .NET
description: Explora las propiedades de DocumentBase para gestionar tus documentos de forma eficiente. ¡Accede a un acceso sin problemas y optimiza tu flujo de trabajo hoy mismo!
type: docs
weight: 20
url: /es/net/aspose.words/documentbase/document/
---
## DocumentBase.Document property

Obtiene esta instancia.

```csharp
public override DocumentBase Document { get; }
```

## Ejemplos

Muestra cómo crear un documento simple.

```csharp
Document doc = new Document();

// Los nuevos objetos de documento vienen por defecto con el conjunto mínimo de nodos
// necesario para comenzar a agregar contenido como texto y formas: una Sección, un Cuerpo y un Párrafo.
doc.AppendChild(new Section(doc))
    .AppendChild(new Body(doc))
    .AppendChild(new Paragraph(doc))
    .AppendChild(new Run(doc, "Hello world!"));
```

### Ver también

* class [DocumentBase](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

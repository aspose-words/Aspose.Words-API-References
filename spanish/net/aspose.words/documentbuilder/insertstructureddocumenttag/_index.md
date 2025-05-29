---
title: DocumentBuilder.InsertStructuredDocumentTag
linktitle: InsertStructuredDocumentTag
articleTitle: InsertStructuredDocumentTag
second_title: Aspose.Words para .NET
description: Mejore sus documentos fácilmente con el método InsertStructuredDocumentTag de DocumentBuilder. ¡Agregue fácilmente etiquetas de documentos estructurados para una mejor organización!
type: docs
weight: 480
url: /es/net/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder.InsertStructuredDocumentTag method

Inserta un[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) en el documento.

```csharp
public StructuredDocumentTag InsertStructuredDocumentTag(SdtType type)
```

### Valor_devuelto

El[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) nodo que acaba de insertarse.

## Ejemplos

Muestra cómo insertar de forma sencilla una etiqueta de documento estructurado.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveTo(doc.FirstSection.Body.Paragraphs[3]);
// Tenga en cuenta que solo se permiten la inserción de los siguientes tipos de StructuredDocumentTag:
// SdtType.Texto sin formato, SdtType.Texto enriquecido, SdtType.Casilla de verificación, SdtType.Lista desplegable,
// SdtType.ComboBox, SdtType.Imagen, SdtType.Fecha.
// El nivel de marcado del StructuredDocumentTag insertado se detectará automáticamente y dependerá de la posición en la que se inserte.
// Se agregó StructuredDocumentTag que heredará el formato de párrafo y fuente de la posición del cursor.
StructuredDocumentTag sdtPlain = builder.InsertStructuredDocumentTag(SdtType.PlainText);

doc.Save(ArtifactsDir + "StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

### Ver también

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* enum [SdtType](../../../aspose.words.markup/sdttype/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---
title: IStructuredDocumentTag.LockContents
linktitle: LockContents
articleTitle: LockContents
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad IStructuredDocumentTag LockContents mejora la seguridad del documento al impedir la edición del contenido. ¡Asegure la integridad de su SDT!
type: docs
weight: 80
url: /es/net/aspose.words.markup/istructureddocumenttag/lockcontents/
---
## IStructuredDocumentTag.LockContents property

Cuando se establece como verdadera, esta propiedad prohibirá que un usuario edite el contenido de esta**TED** .

```csharp
public bool LockContents { get; set; }
```

## Ejemplos

Muestra cómo aplicar restricciones de edición a las etiquetas de documentos estructurados.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta una etiqueta de documento estructurada de texto simple, que actúa como un cuadro de texto que solicita al usuario que lo complete.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Establezca la propiedad "LockContents" en "true" para prohibir que el usuario edite el contenido de este cuadro de texto.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Establezca la propiedad "LockContentControl" en "true" para prohibir al usuario
// eliminar esta etiqueta de documento estructurado manualmente en Microsoft Word.
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### Ver también

* interface [IStructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)

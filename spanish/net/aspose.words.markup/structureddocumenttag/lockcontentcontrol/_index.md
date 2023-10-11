---
title: StructuredDocumentTag.LockContentControl
second_title: Referencia de API de Aspose.Words para .NET
description: StructuredDocumentTag propiedad. Cuando se establece enverdadero  esta propiedad prohibirá a un usuario eliminar esto TED .
type: docs
weight: 190
url: /es/net/aspose.words.markup/structureddocumenttag/lockcontentcontrol/
---
## StructuredDocumentTag.LockContentControl property

Cuando se establece en`verdadero` , esta propiedad prohibirá a un usuario eliminar esto **TED** .

```csharp
public bool LockContentControl { get; set; }
```

### Ejemplos

Muestra cómo aplicar restricciones de edición a etiquetas de documentos estructurados.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta una etiqueta de documento estructurado de texto sin formato, que actúa como un cuadro de texto que solicita al usuario que lo complete.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Establece la propiedad "LockContents" en "true" para prohibir al usuario editar el contenido de este cuadro de texto.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Establece la propiedad "LockContentControl" en "true" para prohibir al usuario
// eliminar esta etiqueta de documento estructurado manualmente en Microsoft Word.
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### Ver también

* class [StructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../structureddocumenttag/)
* asamblea [Aspose.Words](../../../)



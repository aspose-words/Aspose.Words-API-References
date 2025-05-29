---
title: DocumentBuilder.InsertDocumentInline
linktitle: InsertDocumentInline
articleTitle: InsertDocumentInline
second_title: Aspose.Words para .NET
description: Inserte documentos en línea sin esfuerzo con el método InsertDocumentInline de DocumentBuilder, mejorando su flujo de trabajo y su experiencia de edición de documentos.
type: docs
weight: 320
url: /es/net/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder.InsertDocumentInline method

Inserta un documento en línea en la posición del cursor.

```csharp
public Node InsertDocumentInline(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcDoc | Document | Documento fuente para insertar. |
| importFormatMode | ImportFormatMode | Especifica cómo combinar el formato de estilo que entra en conflicto. |
| importFormatOptions | ImportFormatOptions | Permite especificar opciones que afectan el formato de un documento de resultado. |

### Valor_devuelto

Primer nodo del contenido insertado.

## Observaciones

Este método imita el comportamiento de MS Word, como si se presionara CTRL+'A' (seleccionar todo el contenido), luego CTRL+'C' (copiar lo seleccionado en el buffer) dentro de un documento y luego CTRL+'V' (insertar contenido desde el buffer) dentro de otro documento.

A diferencia de[`InsertDocument`](../insertdocument/) Este método mueve el contenido del párrafo del documento de destino, antes del cual se insertó el documento de origen, al último párrafo del documento de origen insertado. Esto significa que se elimina el salto de párrafo del último párrafo insertado.

Tenga en cuenta que si el último nodo del documento fuente no es un párrafo, no se hará nada.

## Ejemplos

Muestra cómo insertar un documento en línea en la posición del cursor.

```csharp
DocumentBuilder srcDoc = new DocumentBuilder();
srcDoc.Write("[src content]");

//Crear documento de destino.
DocumentBuilder dstDoc = new DocumentBuilder();
dstDoc.Write("Before ");
dstDoc.InsertNode(new BookmarkStart(dstDoc.Document, "src_place"));
dstDoc.InsertNode(new BookmarkEnd(dstDoc.Document, "src_place"));
dstDoc.Write(" after");

Assert.AreEqual("Before  after", dstDoc.Document.GetText().TrimEnd());

// Insertar documento de origen en destino en línea.
dstDoc.MoveToBookmark("src_place");
dstDoc.InsertDocumentInline(srcDoc.Document, ImportFormatMode.UseDestinationStyles, new ImportFormatOptions());

Assert.AreEqual("Before [src content] after", dstDoc.Document.GetText().TrimEnd());
```

### Ver también

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---
title: StructuredDocumentTagCollection Class
linktitle: StructuredDocumentTagCollection
articleTitle: StructuredDocumentTagCollection
second_title: Aspose.Words para .NET
description: Explore la clase Aspose.Words.Markup.StructuredDocumentTagCollection para una gestión eficiente de etiquetas de documentos estructurados, mejorando sus capacidades de procesamiento de documentos.
type: docs
weight: 4760
url: /es/net/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class

Una colección de[`IStructuredDocumentTag`](../istructureddocumenttag/) instancias que representan las etiquetas de documento estructurado en el rango especificado.

Para obtener más información, visite el[Etiquetas de documentos estructurados o control de contenido](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Artículo de documentación.

```csharp
public class StructuredDocumentTagCollection : IEnumerable<IStructuredDocumentTag>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.markup/structureddocumenttagcollection/count/) { get; } | Devuelve el número de etiquetas de documentos estructurados en la colección. |
| [Item](../../aspose.words.markup/structureddocumenttagcollection/item/) { get; } | Devuelve la etiqueta del documento estructurado en el índice especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetById](../../aspose.words.markup/structureddocumenttagcollection/getbyid/)(*int*) | Devuelve la etiqueta del documento estructurado por identificador. |
| [GetByTag](../../aspose.words.markup/structureddocumenttagcollection/getbytag/)(*string*) | Devuelve la primera etiqueta de documento estructurado encontrada en la colección con la etiqueta especificada. |
| [GetByTitle](../../aspose.words.markup/structureddocumenttagcollection/getbytitle/)(*string*) | Devuelve la primera etiqueta de documento estructurado encontrada en la colección con el título especificado. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagcollection/getenumerator/)() | Devuelve un objeto enumerador. |
| [Remove](../../aspose.words.markup/structureddocumenttagcollection/remove/)(*int*) | Elimina la etiqueta del documento estructurado con el identificador especificado. |
| [RemoveAt](../../aspose.words.markup/structureddocumenttagcollection/removeat/)(*int*) | Elimina una etiqueta de documento estructurado en el índice especificado. |

## Ejemplos

Muestra cómo obtener la etiqueta de documento estructurado.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Obtener la etiqueta del documento estructurado por Id.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// Obtener la etiqueta del documento estructurado o la etiqueta de rango por título.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Ver también

* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)

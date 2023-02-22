---
title: Class Range
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Range clase. Representa un área contigua en un documento.
type: docs
weight: 4270
url: /es/net/aspose.words/range/
---
## Range class

Representa un área contigua en un documento.

```csharp
public class Range
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Bookmarks](../../aspose.words/range/bookmarks/) { get; } | Devuelve un[`Bookmarks`](./bookmarks/) colección que representa todos los marcadores en el rango. |
| [Fields](../../aspose.words/range/fields/) { get; } | Devuelve un[`Fields`](./fields/) colección que representa todos los campos en el rango. |
| [FormFields](../../aspose.words/range/formfields/) { get; } | Devuelve un[`FormFields`](./formfields/) colección que representa todos los campos de formulario en el rango. |
| [StructuredDocumentTags](../../aspose.words/range/structureddocumenttags/) { get; } | Devuelve un[`StructuredDocumentTags`](./structureddocumenttags/) colección que representa todas las etiquetas de documentos estructurados en el rango. |
| [Text](../../aspose.words/range/text/) { get; } | Obtiene el texto del rango. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Delete](../../aspose.words/range/delete/)() | Borra todos los caracteres del rango. |
| [NormalizeFieldTypes](../../aspose.words/range/normalizefieldtypes/)() | Cambia los valores del tipo de campo[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) de[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) en este rango para que correspondan a los tipos de campo contenidos en los códigos de campo. |
| [Replace](../../aspose.words/range/replace/#replace_2)(Regex, string) | Reemplaza todas las apariciones de un patrón de caracteres especificado por una expresión regular con otra cadena. |
| [Replace](../../aspose.words/range/replace/#replace)(string, string) | Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo. |
| [Replace](../../aspose.words/range/replace/#replace_3)(Regex, string, FindReplaceOptions) | Reemplaza todas las apariciones de un patrón de caracteres especificado por una expresión regular con otra cadena. |
| [Replace](../../aspose.words/range/replace/#replace_1)(string, string, FindReplaceOptions) | Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo. |
| [ToDocument](../../aspose.words/range/todocument/)() | Construye un nuevo documento completamente formado que contiene el rango. |
| [UnlinkFields](../../aspose.words/range/unlinkfields/)() | Desvincula campos en este rango. |
| [UpdateFields](../../aspose.words/range/updatefields/)() | Actualiza los valores de los campos del documento en este rango. |

### Observaciones

El documento está representado por un árbol de nodos y los nodos proporcionan operaciones para trabajar con el árbol, pero algunas operaciones son más fáciles de realizar si el documento se trata como una secuencia contigua de texto.

**Rango** es una interfaz de "fachada" que proporciona métodos que tratan el documento o partes del documento como texto "plano", independientemente del hecho de que los nodos del documento se almacenan en un modelo de objeto similar a un árbol.

**Rango** no contiene ningún texto ni nodos, es simplemente una vista o "ventana" sobre un fragmento de un documento.

### Ejemplos

Muestra cómo obtener el contenido de texto de todos los nodos que cubre un rango.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)



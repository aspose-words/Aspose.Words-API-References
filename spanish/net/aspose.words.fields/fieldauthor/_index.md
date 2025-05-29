---
title: FieldAuthor Class
linktitle: FieldAuthor
articleTitle: FieldAuthor
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fields.FieldAuthor, diseñada para implementar sin esfuerzo el campo AUTOR para una mejor gestión y automatización de documentos.
type: docs
weight: 1980
url: /es/net/aspose.words.fields/fieldauthor/
---
## FieldAuthor class

Implementa el campo AUTOR.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) Artículo de documentación.

```csharp
public class FieldAuthor : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldAuthor](fieldauthor/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AuthorName](../../aspose.words.fields/fieldauthor/authorname/) { get; set; } | Obtiene o establece el nombre del autor del documento. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/)objeto que proporciona acceso tipificado al formato del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que está entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campo. Puede ser`nulo` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado de campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya se ha eliminado, devuelve`nulo` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Realiza la desvinculación del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Realiza la actualización del campo. Se lanza una excepción si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Realiza una actualización de campo. Se lanza una excepción si el campo ya se está actualizando. |

## Observaciones

Recupera y, opcionalmente, establece el nombre del autor del documento, tal como está registrado en el**Autor** propiedad de las propiedades integradas del documento.

## Ejemplos

Muestra cómo utilizar un campo AUTOR para mostrar el nombre del creador de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Los campos AUTOR obtienen sus resultados de la propiedad de documento incorporada llamada "Autor".
// Si creamos y guardamos un documento en Microsoft Word,
//Tendrá nuestro nombre de usuario en esa propiedad.
// Sin embargo, si creamos un documento programáticamente usando Aspose.Words,
// la propiedad "Autor", por defecto, será una cadena vacía.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// Establezca un nombre de autor de respaldo para los campos AUTOR a utilizar
// si la propiedad "Autor" contiene una cadena vacía.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// Actualizar un campo AUTOR que contiene un valor
// aplicará ese valor a la propiedad incorporada "Autor".
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// Cambiar esta propiedad y luego actualizar el campo AUTOR aplicará este valor al campo.
doc.BuiltInDocumentProperties.Author = "John Doe";
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// Si actualizamos un campo AUTOR después de cambiar su propiedad "Nombre",
// luego el campo mostrará el nuevo nombre y aplicará el nuevo nombre a la propiedad incorporada.
field.AuthorName = "Jane Doe";
field.Update();

Assert.AreEqual(" AUTHOR  \"Jane Doe\"", field.GetFieldCode());
Assert.AreEqual("Jane Doe", field.Result);

// Los campos AUTOR no afectan la propiedad DefaultDocumentAuthor.
Assert.AreEqual("Jane Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Joe Bloggs", doc.FieldOptions.DefaultDocumentAuthor);

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)

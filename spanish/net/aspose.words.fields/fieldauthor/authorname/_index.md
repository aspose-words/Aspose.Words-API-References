---
title: FieldAuthor.AuthorName
second_title: Referencia de API de Aspose.Words para .NET
description: FieldAuthor propiedad. Obtiene o establece el nombre del autor del documento.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldauthor/authorname/
---
## FieldAuthor.AuthorName property

Obtiene o establece el nombre del autor del documento.

```csharp
public string AuthorName { get; set; }
```

### Ejemplos

Muestra cómo utilizar un campo AUTOR para mostrar el nombre del creador de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Los campos AUTOR obtienen sus resultados de la propiedad incorporada del documento llamada "Autor".
// Si creamos y guardamos un documento en Microsoft Word,
// tendrá nuestro nombre de usuario en esa propiedad.
// Sin embargo, si creamos un documento mediante programación usando Aspose.Words,
// la propiedad "Autor", por defecto, será una cadena vacía.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// Establece un nombre de autor de copia de seguridad para que se utilicen los campos AUTOR
// si la propiedad "Autor" contiene una cadena vacía.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// Actualizando un campo AUTOR que contiene un valor
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

* class [FieldAuthor](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldauthor/)
* asamblea [Aspose.Words](../../../)



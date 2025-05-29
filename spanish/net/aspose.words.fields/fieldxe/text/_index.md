---
title: FieldXE.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words para .NET
description: Administre fácilmente sus propiedades de texto de FieldXE. Obtenga o configure fácilmente el texto de entrada para una gestión de datos fluida y una experiencia de usuario mejorada.
type: docs
weight: 70
url: /es/net/aspose.words.fields/fieldxe/text/
---
## FieldXE.Text property

Obtiene o establece el texto de la entrada.

```csharp
public string Text { get; set; }
```

## Ejemplos

Muestra cómo crear un campo ÍNDICE y luego usar campos XE para completarlo con entradas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un campo INDEX que mostrará una entrada para cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad Texto del campo XE en el lado izquierdo
// y la página que contiene el campo XE a la derecha.
// Si los campos XE tienen el mismo valor en su propiedad "Texto",
//el campo ÍNDICE los agrupará en una entrada.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Configure el campo INDEX solo para mostrar los campos XE que estén dentro de los límites
// de un marcador llamado "MainBookmark", y cuyas propiedades "EntryType" tienen un valor de "A".
// Para los campos INDEX y XE, la propiedad "EntryType" solo utiliza el primer carácter de su valor de cadena.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// En una nueva página, inicie el marcador con un nombre que coincida con el valor
// de la propiedad "BookmarkName" del campo INDEX.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

//El campo INDEX recogerá esta entrada porque está dentro del marcador,
// y su tipo de entrada también coincide con el tipo de entrada del campo INDEX.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Inserte un campo XE que no aparecerá en el ÍNDICE porque los tipos de entrada no coinciden.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

//Fin del marcador e inserte un campo XE después.
// Es del mismo tipo que el campo INDEX, pero no aparecerá
// ya que está fuera de los límites del marcador.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

Muestra cómo rellenar un campo ÍNDICE con entradas utilizando campos XE y también modificar su apariencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un campo INDEX que mostrará una entrada para cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad de Texto del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// Si los campos XE tienen el mismo valor en su propiedad "Texto",
//el campo ÍNDICE los agrupará en una entrada.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Establecer el valor de esta propiedad en "A" agrupará todas las entradas por su primera letra,
// y coloca esa letra en mayúscula encima de cada grupo.
index.Heading = "A";

// Establezca la tabla creada por el campo INDEX para que abarque 2 columnas.
index.NumberOfColumns = "2";

// Establezca cualquier entrada con letras iniciales fuera del rango de caracteres "ac" para que se omita.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Estos próximos dos campos XE aparecerán bajo el encabezado "A",
// con sus respectivos estilos de texto aplicados también a sus números de página.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";
indexEntry.IsItalic = true;

Assert.AreEqual(" XE  Apple \\i", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apricot";
indexEntry.IsBold = true;

Assert.AreEqual(" XE  Apricot \\b", indexEntry.GetFieldCode());

// Los siguientes dos campos XE estarán bajo un encabezado "B" y "C" en la tabla de contenido de los campos ÍNDICE.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// Los campos ÍNDICE ordenan todas las entradas alfabéticamente, por lo que esta entrada aparecerá debajo de "A" con las otras dos.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

//Esta entrada no aparecerá porque empieza con la letra "D",
// que está fuera del rango de caracteres "ac" que define la propiedad LetterRange del campo INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Ver también

* class [FieldXE](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)

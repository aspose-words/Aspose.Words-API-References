---
title: Text
second_title: Referencia de API de Aspose.Words para .NET
description: Obtiene o establece el texto de la entrada.
type: docs
weight: 70
url: /es/net/aspose.words.fields/fieldxe/text/
---
## FieldXE.Text property

Obtiene o establece el texto de la entrada.

```csharp
public string Text { get; set; }
```

### Ejemplos

Muestra cómo crear un campo ÍNDICE y luego usar campos XE para llenarlo con entradas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un campo ÍNDICE que mostrará una entrada para cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad Texto del campo XE en el lado izquierdo
// y la página que contiene el campo XE a la derecha.
// Si los campos XE tienen el mismo valor en su propiedad "Texto",
// el campo ÍNDICE los agrupará en una sola entrada.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Configure el campo ÍNDICE solo para mostrar los campos XE que están dentro de los límites
// de un marcador llamado "MainBookmark", y cuyas propiedades "EntryType" tienen un valor de "A".
// Para los campos INDEX y XE, la propiedad "EntryType" solo usa el primer carácter de su valor de cadena.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// En una nueva página, comience el marcador con un nombre que coincida con el valor
// de la propiedad "BookmarkName" del campo ÍNDICE.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// El campo ÍNDICE recogerá esta entrada porque está dentro del marcador,
// y su tipo de entrada también coincide con el tipo de entrada del campo ÍNDICE.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Inserte un campo XE que no aparecerá en el ÍNDICE porque los tipos de entrada no coinciden.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Termina el marcador e inserta un campo XE después.
// Es del mismo tipo que el campo ÍNDICE, pero no aparecerá
// ya que está fuera de los límites del marcador.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

Muestra cómo llenar un campo ÍNDICE con entradas usando campos XE y también cómo modificar su apariencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un campo ÍNDICE que mostrará una entrada para cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad Texto del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// Si los campos XE tienen el mismo valor en su propiedad "Texto",
// el campo ÍNDICE los agrupará en una sola entrada.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Establecer el valor de esta propiedad en "A" agrupará todas las entradas por su primera letra,
// y coloca esa letra en mayúscula encima de cada grupo.
index.Heading = "A";

// Configure la tabla creada por el campo ÍNDICE para que abarque 2 columnas.
index.NumberOfColumns = "2";

// Establecer cualquier entrada con letras iniciales fuera del rango de caracteres "ac" para que se omita.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Estos dos campos XE siguientes se mostrarán bajo el encabezado "A",
// con sus respectivos estilos de texto también aplicados a sus números de página.
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

// Los campos ÍNDICE ordenan todas las entradas en orden alfabético, por lo que esta entrada aparecerá debajo de "A" con las otras dos.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Esta entrada no aparecerá porque comienza con la letra "D",
// que está fuera del rango de caracteres "ac" que define la propiedad LetterRange del campo ÍNDICE.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Ver también

* class [FieldXE](../../fieldxe)
* espacio de nombres [Aspose.Words.Fields](../../fieldxe)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

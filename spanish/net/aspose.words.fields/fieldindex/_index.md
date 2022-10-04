---
title: FieldIndex
second_title: Referencia de API de Aspose.Words para .NET
description: Implementa el campo ÍNDICE.
type: docs
weight: 1910
url: /es/net/aspose.words.fields/fieldindex/
---
## FieldIndex class

Implementa el campo ÍNDICE.

```csharp
public class FieldIndex : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldIndex](fieldindex/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldindex/bookmarkname/) { get; set; } | Obtiene o establece el nombre del marcador que marca la parte del documento utilizada para generar el índice. |
| [CrossReferenceSeparator](../../aspose.words.fields/fieldindex/crossreferenceseparator/) { get; set; } | Obtiene o establece la secuencia de caracteres que se utiliza para separar las referencias cruzadas y otras entradas. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [EntryType](../../aspose.words.fields/fieldindex/entrytype/) { get; set; } | Obtiene o establece un tipo de entrada de índice utilizado para crear el índice. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/) objeto que proporciona acceso escrito al formato del campo. |
| [HasPageNumberSeparator](../../aspose.words.fields/fieldindex/haspagenumberseparator/) { get; } | Obtiene un valor que indica si un separador de número de página se anula a través del código del campo. |
| [HasSequenceName](../../aspose.words.fields/fieldindex/hassequencename/) { get; } | Obtiene un valor que indica si se debe usar una secuencia mientras se genera el resultado del campo. |
| [Heading](../../aspose.words.fields/fieldindex/heading/) { get; set; } | Obtiene o establece un encabezado que aparece al comienzo de cada conjunto de entradas para cualquier letra determinada. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LanguageId](../../aspose.words.fields/fieldindex/languageid/) { get; set; } | Obtiene o establece el ID de idioma utilizado para generar el índice. |
| [LetterRange](../../aspose.words.fields/fieldindex/letterrange/) { get; set; } | Obtiene o establece un rango de letras al que limitar el índice. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [NumberOfColumns](../../aspose.words.fields/fieldindex/numberofcolumns/) { get; set; } | Obtiene o establece el número de columnas por página utilizadas al construir el índice. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldindex/pagenumberlistseparator/) { get; set; } | Obtiene o establece la secuencia de caracteres que se utiliza para separar dos números de página en una lista de números de página. |
| [PageNumberSeparator](../../aspose.words.fields/fieldindex/pagenumberseparator/) { get; set; } | Obtiene o establece la secuencia de caracteres que se utiliza para separar una entrada de índice y su número de página. |
| [PageRangeSeparator](../../aspose.words.fields/fieldindex/pagerangeseparator/) { get; set; } | Obtiene o establece la secuencia de caracteres que se utiliza para separar el inicio y el final de un rango de páginas. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [RunSubentriesOnSameLine](../../aspose.words.fields/fieldindex/runsubentriesonsameline/) { get; set; } | Obtiene o establece si se ejecutan subentradas en la misma línea que la entrada principal. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [SequenceName](../../aspose.words.fields/fieldindex/sequencename/) { get; set; } | Obtiene o establece el nombre de una secuencia cuyo número se incluye con el número de página. |
| [SequenceSeparator](../../aspose.words.fields/fieldindex/sequenceseparator/) { get; set; } | Obtiene o establece la secuencia de caracteres que se utiliza para separar números de secuencia y números de página. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |
| [UseYomi](../../aspose.words.fields/fieldindex/useyomi/) { get; set; } | Obtiene o establece si habilitar el uso de yomi text para entradas de índice. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado de campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo principal, devuelve su párrafo principal. Si el campo ya está eliminado, devuelve **nulo** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Realiza el desvinculado del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Realiza la actualización del campo. Se lanza si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Realiza una actualización de campo. Se lanza si el campo ya se está actualizando. |

### Observaciones

Crea un índice utilizando las entradas de índice especificadas por los campos XE e inserta ese índice en este lugar del documento.

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

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

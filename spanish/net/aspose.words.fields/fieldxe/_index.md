---
title: FieldXE
second_title: Referencia de API de Aspose.Words para .NET
description: Implementa el campo XE.
type: docs
weight: 2450
url: /es/net/aspose.words.fields/fieldxe/
---
## FieldXE class

Implementa el campo XE.

```csharp
public class FieldXE : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldXE](fieldxe/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [EntryType](../../aspose.words.fields/fieldxe/entrytype/) { get; set; } | Obtiene o establece un tipo de entrada de índice. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/) objeto que proporciona acceso escrito al formato del campo. |
| [IsBold](../../aspose.words.fields/fieldxe/isbold/) { get; set; } | Obtiene o establece si se aplica el formato de negrita al número de página de la entrada. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsItalic](../../aspose.words.fields/fieldxe/isitalic/) { get; set; } | Obtiene o establece si se aplica el formato de cursiva al número de página de la entrada. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [PageNumberReplacement](../../aspose.words.fields/fieldxe/pagenumberreplacement/) { get; set; } | Obtiene o establece el texto utilizado en lugar de un número de página. |
| [PageRangeBookmarkName](../../aspose.words.fields/fieldxe/pagerangebookmarkname/) { get; set; } | Obtiene o establece el nombre del marcador que marca un rango de páginas que se inserta como número de página de la entrada. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| [Text](../../aspose.words.fields/fieldxe/text/) { get; set; } | Obtiene o establece el texto de la entrada. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |
| [Yomi](../../aspose.words.fields/fieldxe/yomi/) { get; set; } | Obtiene o establece el yomi (primer carácter fonético para ordenar índices) para la entrada de índice |

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

Define el texto y el número de página para una entrada de índice, que es utilizada por un campo ÍNDICE.

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

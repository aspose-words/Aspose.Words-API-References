---
title: FieldSeq Class
linktitle: FieldSeq
articleTitle: FieldSeq
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fields.FieldSeq para una implementación fluida de campos SEQ. Mejore la automatización de sus documentos con potentes funciones y flexibilidad.
type: docs
weight: 2800
url: /es/net/aspose.words.fields/fieldseq/
---
## FieldSeq class

Implementa el campo SEQ.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) Artículo de documentación.

```csharp
public class FieldSeq : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldSeq](fieldseq/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldseq/bookmarkname/) { get; set; } | Obtiene o establece un nombre de marcador que hace referencia a un elemento en otra parte del documento en lugar de en la ubicación actual. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/)objeto que proporciona acceso tipificado al formato del campo. |
| [InsertNextNumber](../../aspose.words.fields/fieldseq/insertnextnumber/) { get; set; } | Obtiene o establece si se debe insertar el siguiente número de secuencia para el elemento especificado. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [ResetHeadingLevel](../../aspose.words.fields/fieldseq/resetheadinglevel/) { get; set; } | Obtiene o establece un número entero que representa un nivel de encabezado al que se restablecerá el número de secuencia. Devuelve -1 si el número está ausente. |
| [ResetNumber](../../aspose.words.fields/fieldseq/resetnumber/) { get; set; } | Obtiene o establece un número entero para restablecer el número de secuencia. Devuelve -1 si el número no está presente. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que está entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campo. Puede ser`nulo` . |
| [SequenceIdentifier](../../aspose.words.fields/fieldseq/sequenceidentifier/) { get; set; } | Obtiene o establece el nombre asignado a la serie de elementos que se van a numerar. |
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

Numera secuencialmente capítulos, tablas, figuras y otras listas de elementos definidas por el usuario en un documento.

## Ejemplos

Muestra la creación de numeración mediante campos SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Los campos SEQ muestran un recuento que se incrementa en cada campo SEQ.
// Estos campos también mantienen recuentos separados para cada secuencia con nombre único
// identificado por la propiedad "SequenceIdentifier" del campo SEQ.
// Inserte un campo SEQ que mostrará el valor de conteo actual de "MySequence",
// después de usar la propiedad "ResetNumber" para establecerlo en 100.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// Muestra el siguiente número en esta secuencia con otro campo SEQ.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// Insertar un encabezado de nivel 1.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Inserte otro campo SEQ de la misma secuencia y configúrelo para restablecer el recuento en cada encabezado con 1.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// El encabezado anterior es un encabezado de nivel 1, por lo que el recuento para esta secuencia se restablece a 1.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// Moverse al siguiente número de esta secuencia.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.InsertNextNumber = true;
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\n", fieldSeq.GetFieldCode());
Assert.AreEqual("2", fieldSeq.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.ResetNumbering.docx");
```

Muestra cómo combinar campos de tabla de contenido y de secuencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un campo TOC puede crear una entrada en su tabla de contenido para cada campo SEQ encontrado en el documento.
// Cada entrada contiene el párrafo que contiene el campo SEQ,
// y el número de la página en la que aparece el campo.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Configure este campo TOC para tener una propiedad SequenceIdentifier con un valor de "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// Configure este campo TOC para seleccionar únicamente los campos SEQ que estén dentro de los límites de un marcador
// llamado "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// Los campos SEQ muestran un recuento que se incrementa en cada campo SEQ.
// Estos campos también mantienen recuentos separados para cada secuencia con nombre único
// identificado por la propiedad "SequenceIdentifier" del campo SEQ.
// Inserte un campo SEQ que tenga un identificador de secuencia que coincida con la tabla de contenidos
// Propiedad TableOfFiguresLabel. Este campo no creará una entrada en la tabla de contenidos, ya que está fuera de ella.
// los límites del marcador designados por "BookmarkName".
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// La secuencia de este campo SEQ coincide con la propiedad "TableOfFiguresLabel" de la tabla de contenidos y está dentro de los límites del marcador.
// El párrafo que contiene este campo aparecerá en la tabla de contenidos como una entrada.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// La secuencia de este campo SEQ no coincide con la propiedad "TableOfFiguresLabel" de la tabla de contenidos.
// y está dentro de los límites del marcador. Su párrafo no aparecerá en la tabla de contenidos como entrada.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// La secuencia de este campo SEQ coincide con la propiedad "TableOfFiguresLabel" de la tabla de contenidos y está dentro de los límites del marcador.
Este campo también hace referencia a otro marcador. El contenido de ese marcador aparecerá en la entrada de la tabla de contenidos de este campo de secuencia.
//El campo SEQ en sí no mostrará el contenido de ese marcador.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Cree un marcador con contenidos que se mostrarán en la entrada TOC debido a que el campo SEQ anterior hace referencia a él.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("SEQBookmark");
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", text from inside SEQBookmark.");
builder.EndBookmark("SEQBookmark");

builder.EndBookmark("TOCBookmark");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.Bookmark.docx");
```

Muestra cómo rellenar un campo TOC con entradas utilizando campos SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un campo TOC puede crear una entrada en su tabla de contenido para cada campo SEQ encontrado en el documento.
// Cada entrada contiene el párrafo que incluye el campo SEQ y el número de página en el que aparece el campo.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Los campos SEQ muestran un recuento que se incrementa en cada campo SEQ.
// Estos campos también mantienen recuentos separados para cada secuencia con nombre único
// identificado por la propiedad "SequenceIdentifier" del campo SEQ.
// Utilice la propiedad "TableOfFiguresLabel" para nombrar una secuencia principal para la tabla de contenidos.
// Ahora, esta tabla de contenidos solo creará entradas a partir de campos SEQ con su "SequenceIdentifier" establecido en "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

//Podemos nombrar otra secuencia del campo SEQ en la propiedad "PrefixedSequenceIdentifier".
 // Los campos SEQ de esta secuencia de prefijo no crearán entradas TOC.
// Cada entrada de TOC creada a partir de un campo SEQ de secuencia principal ahora también mostrará el recuento que
// la secuencia de prefijo está actualmente activada en el campo SEQ de secuencia principal que hizo la entrada.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Cada entrada de TOC mostrará el recuento de la secuencia de prefijo inmediatamente a la izquierda
// del número de página en el que aparece el campo SEQ de secuencia principal.
//Podemos especificar un separador personalizado que aparecerá entre estos dos números.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Hay dos formas de utilizar los campos SEQ para completar esta tabla de contenidos.
// 1 - Insertar un campo SEQ que pertenece a la secuencia de prefijo del TOC:
// Este campo incrementará el recuento de secuencia SEQ para "PrefixSequence" en 1.
// Dado que este campo no pertenece a la secuencia principal identificada
// por la propiedad "TableOfFiguresLabel" del TOC, no aparecerá como una entrada.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Insertar un campo SEQ que pertenece a la secuencia principal del TOC:
//Este campo SEQ creará una entrada en la tabla de contenidos.
// La entrada TOC contendrá el párrafo en el que se encuentra el campo SEQ y el número de la página en la que aparece.
// Esta entrada también mostrará el recuento en el que se encuentra actualmente la secuencia de prefijo.
// separado del número de página por el valor de la propiedad SeqenceSeparator de la tabla de contenidos.
// El recuento de "PrefixSequence" está en 1, este campo SEQ de secuencia principal está en la página 2,
// y el separador es ">", por lo que la entrada mostrará "1>2".
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Inserta una página, avanza la secuencia de prefijo en 2 e inserta un campo SEQ para crear una entrada TOC después.
// La secuencia de prefijo ahora está en 2, y el campo SEQ de secuencia principal está en la página 3,
// por lo que la entrada de TOC mostrará "2>3" en su número de páginas.
builder.InsertBreak(BreakType.PageBreak);
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
builder.Write("Second TOC entry, MySequence #");
fieldSeq.SequenceIdentifier = "MySequence";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TOC.SEQ.docx");
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)

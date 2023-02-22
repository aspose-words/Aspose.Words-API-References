---
title: FieldSeq.SequenceIdentifier
second_title: Referencia de API de Aspose.Words para .NET
description: FieldSeq propiedad. Obtiene o establece el nombre asignado a la serie de elementos que se van a numerar.
type: docs
weight: 60
url: /es/net/aspose.words.fields/fieldseq/sequenceidentifier/
---
## FieldSeq.SequenceIdentifier property

Obtiene o establece el nombre asignado a la serie de elementos que se van a numerar.

```csharp
public string SequenceIdentifier { get; set; }
```

### Ejemplos

Muestra crear numeración usando campos SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Los campos SEQ muestran un recuento que se incrementa en cada campo SEQ.
// Estos campos también mantienen cuentas separadas para cada secuencia nombrada única
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

// Inserta un encabezado de nivel 1.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Inserte otro campo SEQ de la misma secuencia y configúrelo para restablecer el conteo en cada encabezado con 1.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// El encabezado anterior es un encabezado de nivel 1, por lo que el recuento de esta secuencia se restablece a 1.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// Mover al siguiente número de esta secuencia.
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

Muestra cómo llenar un campo TOC con entradas usando campos SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un campo TOC puede crear una entrada en su tabla de contenido para cada campo SEQ encontrado en el documento.
// Cada entrada contiene el párrafo que incluye el campo SEQ y el número de página en el que aparece el campo.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Los campos SEQ muestran un recuento que se incrementa en cada campo SEQ.
// Estos campos también mantienen cuentas separadas para cada secuencia nombrada única
// identificado por la propiedad "SequenceIdentifier" del campo SEQ.
// Use la propiedad "TableOfFiguresLabel" para nombrar una secuencia principal para el TOC.
// Ahora, este TOC solo creará entradas a partir de campos SEQ con su "Identificador de secuencia" establecido en "Mi secuencia".
fieldToc.TableOfFiguresLabel = "MySequence";

// Podemos nombrar otra secuencia de campo SEQ en la propiedad "PrefixedSequenceIdentifier".
  // Los campos SEQ de esta secuencia de prefijos no crearán entradas TOC.
// Cada entrada TOC creada a partir de un campo SEQ de secuencia principal ahora también mostrará el recuento que
// la secuencia de prefijo se encuentra actualmente en el campo SEQ de secuencia principal que realizó la entrada.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Cada entrada de TOC mostrará el conteo de secuencia de prefijo inmediatamente a la izquierda
// del número de página en el que aparece el campo SEQ de la secuencia principal.
// Podemos especificar un separador personalizado que aparecerá entre estos dos números.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Hay dos formas de usar los campos SEQ para completar este TOC.
// 1 - Insertar un campo SEQ que pertenece a la secuencia de prefijos del TOC:
// Este campo incrementará el recuento de secuencias SEQ para "PrefixSequence" en 1.
// Dado que este campo no pertenece a la secuencia principal identificada
// por la propiedad "TableOfFiguresLabel" del TOC, no aparecerá como entrada.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Insertar un campo SEQ que pertenezca a la secuencia principal del TOC:
// Este campo SEQ creará una entrada en la TOC.
// La entrada TOC contendrá el párrafo en el que se encuentra el campo SEQ y el número de la página en la que aparece.
// Esta entrada también mostrará el recuento en el que se encuentra actualmente la secuencia de prefijos,
// separado del número de página por el valor de la propiedad SeqenceSeparator de la tabla de contenido.
// El recuento de "PrefixSequence" está en 1, este campo SEQ de secuencia principal está en la página 2,
// y el separador es ">", por lo que la entrada mostrará "1>2".
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Inserte una página, avance la secuencia del prefijo en 2 e inserte un campo SEQ para crear una entrada TOC después.
// La secuencia del prefijo ahora está en 2, y el campo SEQ de la secuencia principal está en la página 3,
// por lo que la entrada TOC mostrará "2>3" en su recuento de páginas.
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

* class [FieldSeq](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldseq/)
* asamblea [Aspose.Words](../../../)



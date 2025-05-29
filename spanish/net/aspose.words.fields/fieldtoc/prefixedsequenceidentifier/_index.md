---
title: FieldToc.PrefixedSequenceIdentifier
linktitle: PrefixedSequenceIdentifier
articleTitle: PrefixedSequenceIdentifier
second_title: Aspose.Words para .NET
description: Descubra la propiedad PrefixedSequenceIdentifier de FieldToc: administre de manera eficiente los identificadores de secuencia y mejore el número de página de su entrada con prefijos únicos.
type: docs
weight: 120
url: /es/net/aspose.words.fields/fieldtoc/prefixedsequenceidentifier/
---
## FieldToc.PrefixedSequenceIdentifier property

Obtiene o establece el identificador de una secuencia para la cual se debe agregar un prefijo al número de página de la entrada.

```csharp
public string PrefixedSequenceIdentifier { get; set; }
```

## Ejemplos

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

* class [FieldToc](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)

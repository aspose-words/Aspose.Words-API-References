---
title: SequenceSeparator
second_title: Referencia de API de Aspose.Words para .NET
description: Obtiene o establece la secuencia de caracteres que se utiliza para separar números de secuencia y números de página.
type: docs
weight: 150
url: /es/net/aspose.words.fields/fieldtoc/sequenceseparator/
---
## FieldToc.SequenceSeparator property

Obtiene o establece la secuencia de caracteres que se utiliza para separar números de secuencia y números de página.

```csharp
public string SequenceSeparator { get; set; }
```

### Ejemplos

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

* class [FieldToc](../../fieldtoc)
* espacio de nombres [Aspose.Words.Fields](../../fieldtoc)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
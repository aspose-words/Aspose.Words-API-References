---
title: FieldIndex.SequenceSeparator
linktitle: SequenceSeparator
articleTitle: SequenceSeparator
second_title: Aspose.Words para .NET
description: FieldIndex SequenceSeparator propiedad. Obtiene o establece la secuencia de caracteres que se utiliza para separar los números de secuencia y los números de página en C#.
type: docs
weight: 160
url: /es/net/aspose.words.fields/fieldindex/sequenceseparator/
---
## FieldIndex.SequenceSeparator property

Obtiene o establece la secuencia de caracteres que se utiliza para separar los números de secuencia y los números de página.

```csharp
public string SequenceSeparator { get; set; }
```

## Ejemplos

Muestra cómo dividir un documento en porciones combinando los campos ÍNDICE y SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un campo ÍNDICE que mostrará una entrada para cada campo XE que se encuentra en el documento.
// Cada entrada mostrará el valor de la propiedad Texto del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// Si los campos XE tienen el mismo valor en su propiedad "Texto",
// el campo ÍNDICE los agrupará en una sola entrada.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// En la propiedad SequenceName, nombre una secuencia de campo SEQ. Cada entrada de este campo ÍNDICE ahora también se mostrará
// el número en el que se encuentra el recuento de secuencia en la ubicación del campo XE que creó esta entrada.
index.SequenceName = "MySequence";

// Establece el texto que rodeará la secuencia y los números de página para explicar su significado al usuario.
// Una entrada creada con esta configuración mostrará algo como "MiSecuencia en 1 en la página 1" en su número de página.
// PageNumberSeparator y SequenceSeparator no pueden tener más de 15 caracteres.
index.PageNumberSeparator = "\tMySequence at ";
index.SequenceSeparator = " on page ";
Assert.IsTrue(index.HasSequenceName);

Assert.AreEqual(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.GetFieldCode());

// Los campos SEQ muestran un recuento que se incrementa en cada campo SEQ.
// Estos campos también mantienen recuentos separados para cada secuencia con nombre única
// identificado por la propiedad "SequenceIdentifier" del campo SEQ.
// Inserta un campo SEQ que mueve la secuencia "MySequence" a 1.
// Este campo no es diferente del texto normal del documento. No aparecerá en la tabla de contenido de un campo ÍNDICE.
builder.InsertBreak(BreakType.PageBreak);
FieldSeq sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", sequenceField.GetFieldCode());

// Inserta un campo XE que creará una entrada en el campo ÍNDICE.
// Dado que "MySequence" está en 1 y este campo XE está en la página 2, junto con los separadores personalizados que definimos anteriormente,
// la entrada ÍNDICE de este campo mostrará "Cat" en el lado izquierdo y "MySequence en 1 en la página 2" en el derecho.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

Assert.AreEqual(" XE  Cat", indexEntry.GetFieldCode());

// Inserta un salto de página y usa los campos SEQ para avanzar "MySequence" a 3.
builder.InsertBreak(BreakType.PageBreak);
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

// Inserta un campo XE con la misma propiedad de Texto que el anterior.
// La entrada ÍNDICE agrupará los campos XE con valores coincidentes en la propiedad "Texto"
// en una entrada en lugar de hacer una entrada para cada campo XE.
// Dado que estamos en la página 2 con "MySequence" en 3, ", 3 en la página 3" se agregará a la misma entrada ÍNDICE que la anterior.
// La parte del número de página de esa entrada ÍNDICE ahora mostrará "MiSecuencia en 1 en la página 2, 3 en la página 3".
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

// Inserte un campo XE con un valor de propiedad de Texto nuevo y único.
// Esto agregará una nueva entrada, con MySequence en 3 en la página 4.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Dog";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Sequence.docx");
```

### Ver también

* class [FieldIndex](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)

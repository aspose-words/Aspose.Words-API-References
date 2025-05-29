---
title: FieldIndex.HasSequenceName
linktitle: HasSequenceName
articleTitle: HasSequenceName
second_title: Aspose.Words para .NET
description: Descubra si se necesita una secuencia para generar resultados de campo eficientemente con la propiedad FieldIndex HasSequenceName. ¡Optimice su gestión de datos hoy mismo!
type: docs
weight: 60
url: /es/net/aspose.words.fields/fieldindex/hassequencename/
---
## FieldIndex.HasSequenceName property

Obtiene un valor que indica si se debe utilizar una secuencia durante la creación del resultado del campo.

```csharp
public bool HasSequenceName { get; }
```

## Ejemplos

Muestra cómo dividir un documento en partes combinando los campos INDEX y SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un campo INDEX que mostrará una entrada para cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad de Texto del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// Si los campos XE tienen el mismo valor en su propiedad "Texto",
//el campo ÍNDICE los agrupará en una entrada.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

En la propiedad SequenceName, asigne un nombre a una secuencia de campos SEQ. Cada entrada de este campo INDEX ahora también se mostrará.
// el número en el que se encuentra el recuento de secuencia en la ubicación del campo XE que creó esta entrada.
index.SequenceName = "MySequence";

// Establezca el texto que rodeará la secuencia y los números de página para explicar su significado al usuario.
// Una entrada creada con esta configuración mostrará algo como "MySequence en 1 en la página 1" en su número de página.
// PageNumberSeparator y SequenceSeparator no pueden tener más de 15 caracteres.
index.PageNumberSeparator = "\tMySequence at ";
index.SequenceSeparator = " on page ";
Assert.IsTrue(index.HasSequenceName);

Assert.AreEqual(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.GetFieldCode());

// Los campos SEQ muestran un recuento que se incrementa en cada campo SEQ.
// Estos campos también mantienen recuentos separados para cada secuencia con nombre único
// identificado por la propiedad "SequenceIdentifier" del campo SEQ.
// Inserta un campo SEQ que mueve la secuencia "MySequence" a 1.
Este campo no difiere del texto normal del documento. No aparecerá en la tabla de contenido de un campo ÍNDICE.
builder.InsertBreak(BreakType.PageBreak);
FieldSeq sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", sequenceField.GetFieldCode());

// Inserte un campo XE que creará una entrada en el campo ÍNDICE.
// Dado que "MySequence" está en 1 y este campo XE está en la página 2, junto con los separadores personalizados que definimos anteriormente,
// La entrada ÍNDICE de este campo mostrará "Cat" en el lado izquierdo y "MySequence en 1 en la página 2" en el lado derecho.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

Assert.AreEqual(" XE  Cat", indexEntry.GetFieldCode());

// Inserte un salto de página y use los campos SEQ para avanzar "MySequence" a 3.
builder.InsertBreak(BreakType.PageBreak);
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

// Inserte un campo XE con la misma propiedad de Texto que el anterior.
// La entrada INDEX agrupará los campos XE con valores coincidentes en la propiedad "Texto"
// en una sola entrada en lugar de hacer una entrada para cada campo XE.
// Dado que estamos en la página 2 con "MySequence" en 3, ", 3 en la página 3" se agregará a la misma entrada INDEX que la anterior.
// La parte del número de página de esa entrada INDEX ahora mostrará "MySequence en 1 en la página 2, 3 en la página 3".
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

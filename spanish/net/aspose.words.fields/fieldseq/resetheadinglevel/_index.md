---
title: FieldSeq.ResetHeadingLevel
second_title: Referencia de API de Aspose.Words para .NET
description: FieldSeq propiedad. Obtiene o establece un número entero que representa un nivel de encabezado para restablecer el número de secuencia. Devuelve 1 si el número está ausente.
type: docs
weight: 40
url: /es/net/aspose.words.fields/fieldseq/resetheadinglevel/
---
## FieldSeq.ResetHeadingLevel property

Obtiene o establece un número entero que representa un nivel de encabezado para restablecer el número de secuencia. Devuelve -1 si el número está ausente.

```csharp
public string ResetHeadingLevel { get; set; }
```

### Ejemplos

Muestra la numeración creada utilizando campos SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Los campos SEQ muestran un recuento que se incrementa en cada campo SEQ.
// Estos campos también mantienen recuentos separados para cada secuencia con nombre única
// identificado por la propiedad "SequenceIdentifier" del campo SEQ.
// Inserta un campo SEQ que mostrará el valor de recuento actual de "MySequence",
// después de usar la propiedad "ResetNumber" para establecerlo en 100.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// Muestra el siguiente número de esta secuencia con otro campo SEQ.
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

// Inserta otro campo SEQ de la misma secuencia y configúralo para restablecer el recuento en cada encabezado con 1.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// El encabezado anterior es un encabezado de nivel 1, por lo que el recuento de esta secuencia se restablece a 1.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// Pasar al siguiente número de esta secuencia.
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

### Ver también

* class [FieldSeq](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldseq/)
* asamblea [Aspose.Words](../../../)



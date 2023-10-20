---
title: FieldPrint.PostScriptGroup
linktitle: PostScriptGroup
articleTitle: PostScriptGroup
second_title: Aspose.Words para .NET
description: FieldPrint PostScriptGroup propiedad. Obtiene o establece el rectángulo de dibujo en el que operan las instrucciones PostScript en C#.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldprint/postscriptgroup/
---
## FieldPrint.PostScriptGroup property

Obtiene o establece el rectángulo de dibujo en el que operan las instrucciones PostScript.

```csharp
public string PostScriptGroup { get; set; }
```

## Ejemplos

Muestra para insertar un campo PRINT.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

// El campo PRINT puede enviar instrucciones a la impresora.
FieldPrint field = (FieldPrint)builder.InsertField(FieldType.FieldPrint, true);

// Establece el área para que la impresora realice instrucciones.
// En este caso será el párrafo que contiene nuestro campo PRINT.
field.PostScriptGroup = "para";

// Cuando utilizamos una impresora que admite PostScript para imprimir nuestro documento,
// este comando convertirá en blanca toda el área que especificamos en "field.PostScriptGroup".
field.PrinterInstructions = "erasepage";

Assert.AreEqual(" PRINT  erasepage \\p para", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### Ver también

* class [FieldPrint](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)

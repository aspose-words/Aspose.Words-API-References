---
title: FieldPrint.PrinterInstructions
linktitle: PrinterInstructions
articleTitle: PrinterInstructions
second_title: Aspose.Words para .NET
description: FieldPrint PrinterInstructions propiedad. Obtiene o establece los caracteres del código de control específicos de la impresora o las instrucciones PostScript en C#.
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldprint/printerinstructions/
---
## FieldPrint.PrinterInstructions property

Obtiene o establece los caracteres del código de control específicos de la impresora o las instrucciones PostScript.

```csharp
public string PrinterInstructions { get; set; }
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

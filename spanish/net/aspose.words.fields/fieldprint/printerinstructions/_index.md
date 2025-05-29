---
title: FieldPrint.PrinterInstructions
linktitle: PrinterInstructions
articleTitle: PrinterInstructions
second_title: Aspose.Words para .NET
description: Descubra cómo administrar códigos de control específicos de la impresora e instrucciones PostScript con FieldPrint PrinterInstructions para obtener soluciones de impresión optimizadas.
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

Muestra cómo insertar un campo IMPRESIÓN.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

//El campo PRINT puede enviar instrucciones a la impresora.
FieldPrint field = (FieldPrint)builder.InsertField(FieldType.FieldPrint, true);

// Establezca el área donde la impresora ejecutará instrucciones.
// En este caso será el párrafo que contenga nuestro campo PRINT.
field.PostScriptGroup = "para";

// Cuando utilizamos una impresora que admite PostScript para imprimir nuestro documento,
// este comando volverá blanca toda el área que especificamos en "field.PostScriptGroup".
field.PrinterInstructions = "erasepage";

Assert.AreEqual(" PRINT  erasepage \\p para", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### Ver también

* class [FieldPrint](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)

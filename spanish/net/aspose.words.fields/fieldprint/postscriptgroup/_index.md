---
title: FieldPrint.PostScriptGroup
linktitle: PostScriptGroup
articleTitle: PostScriptGroup
second_title: Aspose.Words para .NET
description: Descubra la propiedad PostScriptGroup FieldPrint para administrar fácilmente su rectángulo de dibujo para un manejo eficiente de las instrucciones PostScript.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldprint/postscriptgroup/
---
## FieldPrint.PostScriptGroup property

Obtiene o establece el rectángulo de dibujo sobre el que operan las instrucciones PostScript.

```csharp
public string PostScriptGroup { get; set; }
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

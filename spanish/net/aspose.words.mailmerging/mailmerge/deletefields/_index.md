---
title: MailMerge.DeleteFields
second_title: Referencia de API de Aspose.Words para .NET
description: MailMerge método. Elimina los campos relacionados con la combinación de correspondencia del documento.
type: docs
weight: 170
url: /es/net/aspose.words.mailmerging/mailmerge/deletefields/
---
## MailMerge.DeleteFields method

Elimina los campos relacionados con la combinación de correspondencia del documento.

```csharp
public void DeleteFields()
```

### Observaciones

Este método elimina los campos MERGEFIELD y NEXT del documento.

Este método podría resultar útil si su operación de combinación de correspondencia no siempre necesita para completar todos los campos del documento. Utilice este método para eliminar todos los campos de combinación de correspondencia restantes.

### Ejemplos

Muestra cómo eliminar todos los MERGEFIELD de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.Writeln(",");
builder.Writeln("Greetings!");

Assert.AreEqual(
    "Dear \u0013 MERGEFIELD FirstName \u0014«FirstName»\u0015 \u0013 MERGEFIELD LastName \u0014«LastName»\u0015,\rGreetings!", 
    doc.GetText().Trim());

doc.MailMerge.DeleteFields();

Assert.AreEqual("Dear  ,\rGreetings!", doc.GetText().Trim());
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../mailmerge/)
* asamblea [Aspose.Words](../../../)



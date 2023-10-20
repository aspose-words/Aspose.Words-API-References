---
title: FieldMergingArgsBase.FieldValue
linktitle: FieldValue
articleTitle: FieldValue
second_title: Aspose.Words para .NET
description: FieldMergingArgsBase FieldValue propiedad. Obtiene o establece el valor del campo del origen de datos en C#.
type: docs
weight: 50
url: /es/net/aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/
---
## FieldMergingArgsBase.FieldValue property

Obtiene o establece el valor del campo del origen de datos.

```csharp
public object FieldValue { get; set; }
```

## Observaciones

Esta propiedad contiene un valor que el motor de combinación de correspondencia acaba de seleccionar de su fuente de datos para este campo. También puede reemplazar el valor configurando la propiedad.

## Ejemplos

Muestra cómo editar los valores que reciben los MERGEFIELD cuando se realiza una combinación de correspondencia.

```csharp
public void FieldFormats()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inserte algunos MERGEFIELD con cambios de formato que editarán los valores que recibirán durante una combinación de correspondencia.
    builder.InsertField("MERGEFIELD text_Field1 \\* Caps", null);
    builder.Write(", ");
    builder.InsertField("MERGEFIELD text_Field2 \\* Upper", null);
    builder.Write(", ");
    builder.InsertField("MERGEFIELD numeric_Field1 \\# 0.0", null);

    builder.Document.MailMerge.FieldMergingCallback = new FieldValueMergingCallback();

    builder.Document.MailMerge.Execute(
        new string[] { "text_Field1", "text_Field2", "numeric_Field1" },
        new object[] { "Field 1", "Field 2", 10 });
    string t = doc.GetText().Trim();
    Assert.AreEqual("Merge Value For \"Text_Field1\": Field 1, MERGE VALUE FOR \"TEXT_FIELD2\": FIELD 2, 10000.0", doc.GetText().Trim());
}

/// <summary>
/// Edita los valores que reciben los MERGEFIELD durante una combinación de correspondencia.
/// El nombre de un MERGEFIELD debe tener un prefijo para que esta devolución de llamada surta efecto en su valor.
/// </summary>
private class FieldValueMergingCallback : IFieldMergingCallback
{
    /// <summary>
    /// Se llama cuando una combinación de correspondencia combina datos en un MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs e)
    {
        if (e.FieldName.StartsWith("text_"))
            e.FieldValue = $"Merge value for \"{e.FieldName}\": {(string)e.FieldValue}";
        else if (e.FieldName.StartsWith("numeric_"))
            e.FieldValue = (int)e.FieldValue * 1000;
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        // Hacer nada.
    }
}
```

### Ver también

* class [FieldMergingArgsBase](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)

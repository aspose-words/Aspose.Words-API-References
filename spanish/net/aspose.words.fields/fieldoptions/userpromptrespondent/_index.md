---
title: FieldOptions.UserPromptRespondent
second_title: Referencia de API de Aspose.Words para .NET
description: FieldOptions propiedad. Obtiene o configura al encuestado para las indicaciones del usuario durante la actualización del campo.
type: docs
weight: 200
url: /es/net/aspose.words.fields/fieldoptions/userpromptrespondent/
---
## FieldOptions.UserPromptRespondent property

Obtiene o configura al encuestado para las indicaciones del usuario durante la actualización del campo.

```csharp
public IFieldUserPromptRespondent UserPromptRespondent { get; set; }
```

### Observaciones

Si el valor de esta propiedad se establece en **nulo** , los campos que requieren respuesta del usuario en prompting (como[`FieldAsk`](../../fieldask/) o[`FieldFillIn`](../../fieldfillin/)) no están actualizados.

El valor predeterminado es **nulo**.

### Ejemplos

Muestra cómo crear un campo ASK y establecer sus propiedades.

```csharp
[Test]
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Coloque un campo donde se colocará la respuesta a nuestro campo ASK.
    FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    fieldRef.BookmarkName = "MyAskField";
    builder.Writeln();

    Assert.AreEqual(" REF  MyAskField", fieldRef.GetFieldCode());

    // Inserte el campo ASK y edite sus propiedades para hacer referencia a nuestro campo REF por nombre de marcador.
    FieldAsk fieldAsk = (FieldAsk)builder.InsertField(FieldType.FieldAsk, true);
    fieldAsk.BookmarkName = "MyAskField";
    fieldAsk.PromptText = "Please provide a response for this ASK field";
    fieldAsk.DefaultResponse = "Response from within the field.";
    fieldAsk.PromptOnceOnMailMerge = true;
    builder.Writeln();

    Assert.AreEqual(
        " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
        fieldAsk.GetFieldCode());

    // Los campos ASK aplican la respuesta predeterminada a sus respectivos campos REF durante una combinación de correspondencia.
    DataTable table = new DataTable("My Table");
    table.Columns.Add("Column 1");
    table.Rows.Add("Row 1");
    table.Rows.Add("Row 2");

    FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    fieldMergeField.FieldName = "Column 1";

    // Podemos modificar o anular la respuesta predeterminada en nuestros campos ASK con un contestador personalizado,
    // que ocurrirá durante una combinación de correspondencia.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");

/// <summary>
/// Antepone texto a la respuesta predeterminada de un campo ASK durante una combinación de correspondencia.
/// </summary>
private class MyPromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response from MyPromptRespondent. " + defaultResponse;
    }
}
```

### Ver también

* interface [IFieldUserPromptRespondent](../../ifielduserpromptrespondent/)
* class [FieldOptions](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldoptions/)
* asamblea [Aspose.Words](../../../)



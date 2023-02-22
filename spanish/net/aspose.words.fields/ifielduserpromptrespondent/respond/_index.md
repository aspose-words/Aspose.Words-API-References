---
title: IFieldUserPromptRespondent.Respond
second_title: Referencia de API de Aspose.Words para .NET
description: IFieldUserPromptRespondent método. Cuando se implementa devuelve una respuesta del usuario al solicitarlo. Su implementación debería devolver nulo para indicar que el usuario no respondió al aviso es decir el usuario presionó el botón Cancelar en la ventana del aviso.
type: docs
weight: 10
url: /es/net/aspose.words.fields/ifielduserpromptrespondent/respond/
---
## IFieldUserPromptRespondent.Respond method

Cuando se implementa, devuelve una respuesta del usuario al solicitarlo. Su implementación debería devolver **nulo** para indicar que el usuario no respondió al aviso (es decir, el usuario presionó el botón Cancelar en la ventana del aviso).

```csharp
public string Respond(string promptText, string defaultResponse)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| promptText | String | Texto de solicitud (es decir, título de la ventana de solicitud). |
| defaultResponse | String | Respuesta de usuario predeterminada (es decir, valor inicial contenido en la ventana de solicitud). |

### Valor_devuelto

Respuesta del usuario (es decir, valor confirmado contenido en la ventana de solicitud).

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

* interface [IFieldUserPromptRespondent](../)
* espacio de nombres [Aspose.Words.Fields](../../ifielduserpromptrespondent/)
* asamblea [Aspose.Words](../../../)



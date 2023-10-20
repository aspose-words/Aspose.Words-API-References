---
title: FieldAsk.PromptText
linktitle: PromptText
articleTitle: PromptText
second_title: Aspose.Words para .NET
description: FieldAsk PromptText propiedad. Obtiene o establece el texto del mensaje el título de la ventana del mensaje en C#.
type: docs
weight: 50
url: /es/net/aspose.words.fields/fieldask/prompttext/
---
## FieldAsk.PromptText property

Obtiene o establece el texto del mensaje (el título de la ventana del mensaje).

```csharp
public string PromptText { get; set; }
```

## Ejemplos

Muestra cómo crear un campo ASK y establecer sus propiedades.

```csharp
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Colocar un campo donde se colocará la respuesta a nuestro campo ASK.
    FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    fieldRef.BookmarkName = "MyAskField";
    builder.Writeln();

    Assert.AreEqual(" REF  MyAskField", fieldRef.GetFieldCode());

    // Inserte el campo ASK y edite sus propiedades para hacer referencia a nuestro campo REF por el nombre del marcador.
    FieldAsk fieldAsk = (FieldAsk)builder.InsertField(FieldType.FieldAsk, true);
    fieldAsk.BookmarkName = "MyAskField";
    fieldAsk.PromptText = "Please provide a response for this ASK field";
    fieldAsk.DefaultResponse = "Response from within the field.";
    fieldAsk.PromptOnceOnMailMerge = true;
    builder.Writeln();

    Assert.AreEqual(
        " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
        fieldAsk.GetFieldCode());

    // Los campos PREGUNTAR aplican la respuesta predeterminada a sus respectivos campos REF durante una combinación de correspondencia.
    DataTable table = new DataTable("My Table");
    table.Columns.Add("Column 1");
    table.Rows.Add("Row 1");
    table.Rows.Add("Row 2");

    FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    fieldMergeField.FieldName = "Column 1";

    // Podemos modificar o anular la respuesta predeterminada en nuestros campos PREGUNTAR con un respondedor personalizado,
    // que ocurrirá durante una combinación de correspondencia.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");
}

/// <summary>
/// Antepone texto a la respuesta predeterminada de un campo PREGUNTAR durante una combinación de correspondencia.
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

* class [FieldAsk](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)

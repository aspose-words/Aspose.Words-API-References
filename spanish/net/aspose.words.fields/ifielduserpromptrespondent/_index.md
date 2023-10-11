---
title: Interface IFieldUserPromptRespondent
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fields.IFieldUserPromptRespondent interfaz. Representa al encuestado ante las indicaciones del usuario durante la actualización del campo.
type: docs
weight: 2740
url: /es/net/aspose.words.fields/ifielduserpromptrespondent/
---
## IFieldUserPromptRespondent interface

Representa al encuestado ante las indicaciones del usuario durante la actualización del campo.

```csharp
public interface IFieldUserPromptRespondent
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Respond](../../aspose.words.fields/ifielduserpromptrespondent/respond/)(string, string) | Cuando se implementa, devuelve una respuesta del usuario cuando se le solicita. Su implementación debería devolver`nulo` para indicar que el usuario no ha respondido al mensaje (es decir, el usuario ha presionado el botón Cancelar en la ventana del mensaje). |

### Observaciones

Los campos PREGUNTAR y FILLIN son ejemplos de campos que solicitan al usuario alguna respuesta. Implemente esta interfaz y asígnela al[`UserPromptRespondent`](../fieldoptions/userpromptrespondent/) propiedad para establecer la interacción entre el campo update y el usuario.

### Ejemplos

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

* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)



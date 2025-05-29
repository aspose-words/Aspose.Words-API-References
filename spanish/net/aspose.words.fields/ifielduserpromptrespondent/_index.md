---
title: IFieldUserPromptRespondent Interface
linktitle: IFieldUserPromptRespondent
articleTitle: IFieldUserPromptRespondent
second_title: Aspose.Words para .NET
description: Descubra la interfaz Aspose.Words.Fields.IFieldUserPromptRespondent, diseñada para mejorar la interacción del usuario y agilizar las actualizaciones de campos sin problemas.
type: docs
weight: 3150
url: /es/net/aspose.words.fields/ifielduserpromptrespondent/
---
## IFieldUserPromptRespondent interface

Representa al encuestado ante las solicitudes del usuario durante la actualización del campo.

```csharp
public interface IFieldUserPromptRespondent
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Respond](../../aspose.words.fields/ifielduserpromptrespondent/respond/)(*string, string*) | Cuando se implementa, devuelve una respuesta del usuario al solicitarlo. Su implementación debería devolver`nulo` para indicar que el usuario no ha respondido al mensaje (es decir, el usuario ha presionado el botón Cancelar en la ventana del mensaje). |

## Observaciones

Los campos ASK y FILLIN son ejemplos de campos que solicitan al usuario una respuesta. Implemente esta interfaz y asígnela a[`UserPromptRespondent`](../fieldoptions/userpromptrespondent/) propiedad para establecer interacción entre el campo update y el usuario.

## Ejemplos

Muestra cómo crear un campo ASK y configurar sus propiedades.

```csharp
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    //Coloca un campo donde se colocará la respuesta a nuestro campo ASK.
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

    // Podemos modificar o anular la respuesta predeterminada en nuestros campos ASK con un respondedor de solicitud personalizado,
    // que ocurrirá durante una combinación de correspondencia.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");
}

/// <summary>
/// Agrega texto al comienzo de la respuesta predeterminada de un campo ASK durante una combinación de correspondencia.
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

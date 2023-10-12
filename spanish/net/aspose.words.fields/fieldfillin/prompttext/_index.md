---
title: FieldFillIn.PromptText
second_title: Referencia de API de Aspose.Words para .NET
description: FieldFillIn propiedad. Obtiene o establece el texto del mensaje el título de la ventana del mensaje.
type: docs
weight: 40
url: /es/net/aspose.words.fields/fieldfillin/prompttext/
---
## FieldFillIn.PromptText property

Obtiene o establece el texto del mensaje (el título de la ventana del mensaje).

```csharp
public string PromptText { get; set; }
```

### Ejemplos

Muestra cómo utilizar el campo FILLIN para solicitar una respuesta al usuario.

```csharp
public void FieldFillIn()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Insertar un campo FILLIN. Cuando actualizamos manualmente este campo en Microsoft Word,
    // nos pedirá que ingresemos una respuesta. El campo luego mostrará la respuesta como texto.
    FieldFillIn field = (FieldFillIn)builder.InsertField(FieldType.FieldFillIn, true);
    field.PromptText = "Please enter a response:";
    field.DefaultResponse = "A default response.";

    // También podemos usar estos campos para pedirle al usuario una respuesta única para cada página
    // creado durante una combinación de correspondencia realizada con Microsoft Word.
    field.PromptOnceOnMailMerge = true;

    Assert.AreEqual(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.GetFieldCode());

    FieldMergeField mergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    mergeField.FieldName = "MergeField";

    // Si realizamos una combinación de correspondencia mediante programación, podemos utilizar un encuestado personalizado
    // para editar automáticamente las respuestas de los campos FILLIN que encuentra la combinación de correspondencia.
    doc.FieldOptions.UserPromptRespondent = new PromptRespondent();
    doc.MailMerge.Execute(new [] { "MergeField" }, new object[] { "" });

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.FILLIN.docx");
}

/// <summary>
/// Antepone una línea a la respuesta predeterminada de cada campo FILLIN durante una combinación de correspondencia.
/// </summary>
private class PromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response modified by PromptRespondent. " + defaultResponse;
    }
}
```

### Ver también

* class [FieldFillIn](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldfillin/)
* asamblea [Aspose.Words](../../../)



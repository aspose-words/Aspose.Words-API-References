---
title: FieldFillIn
second_title: Referencia de API de Aspose.Words para .NET
description: Implementa el campo RELLENO.
type: docs
weight: 1740
url: /es/net/aspose.words.fields/fieldfillin/
---
## FieldFillIn class

Implementa el campo RELLENO.

```csharp
public class FieldFillIn : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldFillIn](fieldfillin)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DefaultResponse](../../aspose.words.fields/fieldfillin/defaultresponse) { get; set; } | Obtiene o establece la respuesta del usuario predeterminada (valor inicial contenido en la ventana de solicitud). |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format) { get; } | Obtiene un[`FieldFormat`](../fieldformat) objeto que proporciona acceso escrito al formato del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Obtiene o establece el LCID del campo. |
| [PromptOnceOnMailMerge](../../aspose.words.fields/fieldfillin/promptonceonmailmerge) { get; set; } | Obtiene o establece si la respuesta del usuario debe recibirse una vez por operación de combinación de correspondencia. |
| [PromptText](../../aspose.words.fields/fieldfillin/prompttext) { get; set; } | Obtiene o establece el texto de solicitud (el título de la ventana de solicitud). |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [Start](../../aspose.words.fields/field/start) { get; } | Obtiene el nodo que representa el inicio del campo. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Obtiene el tipo de campo de Microsoft Word. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado de campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo principal, devuelve su párrafo principal. Si el campo ya está eliminado, devuelve **nulo** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Realiza el desvinculado del campo. |
| [Update](../../aspose.words.fields/field/update)() | Realiza la actualización del campo. Se lanza si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update)(bool) | Realiza una actualización de campo. Se lanza si el campo ya se está actualizando. |

### Observaciones

Solicita al usuario que ingrese texto.

### Ejemplos

Muestra cómo utilizar el campo FILLIN para solicitar una respuesta al usuario.

```csharp
public void FieldFillIn()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Insertar un campo de LLENADO. Cuando actualizamos manualmente este campo en Microsoft Word,
    // nos pedirá que ingresemos una respuesta. El campo mostrará la respuesta como texto.
    FieldFillIn field = (FieldFillIn)builder.InsertField(FieldType.FieldFillIn, true);
    field.PromptText = "Please enter a response:";
    field.DefaultResponse = "A default response.";

    // También podemos usar estos campos para pedirle al usuario una respuesta única para cada página
    // creado durante una combinación de correspondencia realizada con Microsoft Word.
    field.PromptOnceOnMailMerge = true;

    Assert.AreEqual(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.GetFieldCode());

    FieldMergeField mergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    mergeField.FieldName = "MergeField";

    // Si realizamos una combinación de correo programáticamente, podemos usar un encuestado personalizado
    // para editar automáticamente las respuestas de los campos FILLIN que encuentra la combinación de correspondencia.
    doc.FieldOptions.UserPromptRespondent = new PromptRespondent();
    doc.MailMerge.Execute(new [] { "MergeField" }, new object[] { "" });

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.FILLIN.docx");

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

* class [Field](../field)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

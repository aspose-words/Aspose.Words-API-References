---
title: FieldUpdatingProgressArgs.UpdatedFieldsCount
linktitle: UpdatedFieldsCount
articleTitle: UpdatedFieldsCount
second_title: Aspose.Words para .NET
description: Descubra la propiedad UpdatedFieldsCount de FieldUpdatingProgressArgs para rastrear fácilmente la cantidad de campos actualizados en su aplicación.
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldupdatingprogressargs/updatedfieldscount/
---
## FieldUpdatingProgressArgs.UpdatedFieldsCount property

Obtiene el número de campos actualizados.

```csharp
public int UpdatedFieldsCount { get; }
```

## Ejemplos

Muestra cómo utilizar métodos de devolución de llamada durante una actualización de campo.

```csharp
public void FieldUpdatingCallbackTest()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder.InsertField(" TIME ");
    builder.InsertField(" REVNUM ");
    builder.InsertField(" AUTHOR  \"John Doe\" ");
    builder.InsertField(" SUBJECT \"My Subject\" ");
    builder.InsertField(" QUOTE \"Hello world!\" ");

    FieldUpdatingCallback callback = new FieldUpdatingCallback();
    doc.FieldOptions.FieldUpdatingCallback = callback;

    doc.UpdateFields();

    Assert.True(callback.FieldUpdatedCalls.Contains("Updating John Doe"));
}

/// <summary>
/// Implemente esta interfaz si desea que sus propios métodos personalizados sean llamados durante una actualización de campo.
/// </summary>
public class FieldUpdatingCallback : IFieldUpdatingCallback, IFieldUpdatingProgressCallback
{
    public FieldUpdatingCallback()
    {
        FieldUpdatedCalls = new List<string>();
    }

    /// <summary>
    /// Un método definido por el usuario que se llama justo antes de que se actualice un campo.
    /// </summary>
    void IFieldUpdatingCallback.FieldUpdating(Field field)
    {
        if (field.Type == FieldType.FieldAuthor)
        {
            FieldAuthor fieldAuthor = (FieldAuthor) field;
            fieldAuthor.AuthorName = "Updating John Doe";
        }
    }

    /// <summary>
    /// Un método definido por el usuario que se llama justo después de que se actualiza un campo.
    /// </summary>
    void IFieldUpdatingCallback.FieldUpdated(Field field)
    {
        FieldUpdatedCalls.Add(field.Result);
    }

    void IFieldUpdatingProgressCallback.Notify(FieldUpdatingProgressArgs args)
    {
        Console.WriteLine($"{args.UpdateCompleted}/{args.TotalFieldsCount}");
        Console.WriteLine($"{args.UpdatedFieldsCount}");
    }

    public IList<string> FieldUpdatedCalls { get; }
}
```

### Ver también

* class [FieldUpdatingProgressArgs](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)

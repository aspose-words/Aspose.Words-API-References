---
title: IFieldUpdatingProgressCallback.Notify
linktitle: Notify
articleTitle: Notify
second_title: .NET için Aspose.Words
description: İlerleme güncellemelerini etkin bir şekilde izlemek ve yanıtlamak için tasarlanmış IFieldUpdatingProgressCallback Notify yöntemiyle uygulamanızın performansını artırın.
type: docs
weight: 10
url: /tr/net/aspose.words.fields/ifieldupdatingprogresscallback/notify/
---
## IFieldUpdatingProgressCallback.Notify method

İlerleme güncellendiğinde çağrılan kullanıcı tanımlı bir yöntem.

```csharp
public void Notify(FieldUpdatingProgressArgs args)
```

## Örnekler

Bir alan güncellemesi sırasında geri çağırma yöntemlerinin nasıl kullanılacağını gösterir.

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
/// Bir alan güncellemesi sırasında kendi özel yöntemlerinizin çağrılmasını istiyorsanız bu arayüzü uygulayın.
/// </summary>
public class FieldUpdatingCallback : IFieldUpdatingCallback, IFieldUpdatingProgressCallback
{
    public FieldUpdatingCallback()
    {
        FieldUpdatedCalls = new List<string>();
    }

    /// <summary>
    /// Bir alan güncellenmeden hemen önce çağrılan kullanıcı tanımlı bir yöntem.
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
    /// Bir alan güncellendikten hemen sonra çağrılan kullanıcı tanımlı bir yöntem.
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

### Ayrıca bakınız

* class [FieldUpdatingProgressArgs](../../fieldupdatingprogressargs/)
* interface [IFieldUpdatingProgressCallback](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

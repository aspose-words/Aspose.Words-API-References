---
title: IFieldUpdatingCallback.FieldUpdated
second_title: Aspose.Words for .NET API Referansı
description: IFieldUpdatingCallback yöntem. Bir alan güncellendikten hemen sonra çağrılan kullanıcı tanımlı bir yöntem.
type: docs
weight: 10
url: /tr/net/aspose.words.fields/ifieldupdatingcallback/fieldupdated/
---
## IFieldUpdatingCallback.FieldUpdated method

Bir alan güncellendikten hemen sonra çağrılan kullanıcı tanımlı bir yöntem.

```csharp
public void FieldUpdated(Field field)
```

### Örnekler

Bir alan güncellemesi sırasında geri arama yöntemlerinin nasıl kullanılacağını gösterir.

```csharp
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
public class FieldUpdatingCallback : IFieldUpdatingCallback
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

    public IList<string> FieldUpdatedCalls { get; }
}
```

### Ayrıca bakınız

* class [Field](../../field/)
* interface [IFieldUpdatingCallback](../)
* ad alanı [Aspose.Words.Fields](../../ifieldupdatingcallback/)
* toplantı [Aspose.Words](../../../)



---
title: FieldOptions.FieldUpdatingCallback
linktitle: FieldUpdatingCallback
articleTitle: FieldUpdatingCallback
second_title: .NET için Aspose.Words
description: IFieldUpdatingCallback uygulamalarını kolayca yönetmek ve veri işleme verimliliğinizi artırmak için FieldOptions FieldUpdatingCallback özelliğini keşfedin.
type: docs
weight: 120
url: /tr/net/aspose.words.fields/fieldoptions/fieldupdatingcallback/
---
## FieldOptions.FieldUpdatingCallback property

Alır veya ayarlar[`IFieldUpdatingCallback`](../../ifieldupdatingcallback/) uygulama

```csharp
public IFieldUpdatingCallback FieldUpdatingCallback { get; set; }
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

* interface [IFieldUpdatingCallback](../../ifieldupdatingcallback/)
* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

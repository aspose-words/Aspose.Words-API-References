---
title: FieldUpdatingProgressArgs Class
linktitle: FieldUpdatingProgressArgs
articleTitle: FieldUpdatingProgressArgs
second_title: .NET için Aspose.Words
description: Alan ilerlemesi hakkında gerçek zamanlı güncellemeler sağlayarak belge otomasyonunuzu geliştiren Aspose.Words.Fields.FieldUpdatingProgressArgs sınıfını keşfedin.
type: docs
weight: 2980
url: /tr/net/aspose.words.fields/fieldupdatingprogressargs/
---
## FieldUpdatingProgressArgs class

Alan güncelleme ilerleme olayı için veri sağlar.

```csharp
public sealed class FieldUpdatingProgressArgs
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [TotalFieldsCount](../../aspose.words.fields/fieldupdatingprogressargs/totalfieldscount/) { get; } | Güncellenecek toplam alan sayısını alır. |
| [UpdateCompleted](../../aspose.words.fields/fieldupdatingprogressargs/updatecompleted/) { get; } | Alan güncellemesinin tamamlanıp tamamlanmadığını belirten bir değer alır. |
| [UpdatedFieldsCount](../../aspose.words.fields/fieldupdatingprogressargs/updatedfieldscount/) { get; } | Güncellenen alanların sayısını alır. |

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

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)

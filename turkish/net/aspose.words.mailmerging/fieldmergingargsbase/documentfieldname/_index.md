---
title: FieldMergingArgsBase.DocumentFieldName
linktitle: DocumentFieldName
articleTitle: DocumentFieldName
second_title: .NET için Aspose.Words
description: FieldMergingArgsBase'in DocumentFieldName özelliğini keşfedin. Verimli belge işleme için birleştirme alanı adlarına kolayca erişin ve bunları yönetin.
type: docs
weight: 20
url: /tr/net/aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/
---
## FieldMergingArgsBase.DocumentFieldName property

Belgede belirtilen birleştirme alanının adını alır.

```csharp
public string DocumentFieldName { get; }
```

## Notlar

Bir belge alan adından farklı bir veri kaynağı alan adına eşlemeniz varsa, bu, belgede belirtilen orijinal alan adıdır.

Örneğin belgede "Image:MyFieldName" gibi bir alan adı öneki belirttiyseniz, o zaman`DocumentFieldName` önek olmadan alan adını, yani "MyFieldName"i döndürür.

## Örnekler

HTML belgeleri biçiminde birleştirme verilerini işleyen özel bir geri aramayla bir posta birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
public void MergeHtml()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(@"MERGEFIELD  html_Title  \b Content");
    builder.InsertField(@"MERGEFIELD  html_Body  \b Content");

    object[] mergeData =
    {
        "<html>" +
            "<h1>" +
                "<span style=\"color: #0000ff; font-family: Arial;\">Hello World!</span>" +
            "</h1>" +
        "</html>", 

        "<html>" +
            "<blockquote>" +
                "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>" +
            "</blockquote>" +
        "</html>"
    };

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldInsertHtml();
    doc.MailMerge.Execute(new[] { "html_Title", "html_Body" }, mergeData);

    doc.Save(ArtifactsDir + "MailMergeEvent.MergeHtml.docx");
}

/// <summary>
/// Posta birleştirme işlemi, adı "html_" önekiyle başlayan bir MERGEFIELD ile karşılaşırsa,
/// bu geri çağırma birleştirme verilerini HTML içeriği olarak ayrıştırır ve sonucu MERGEFIELD'ın belge konumuna ekler.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// Bir posta birleştirme işlemi verileri bir MERGEFIELD'a birleştirdiğinde çağrılır.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // Ayrıştırılmış HTML verilerini belgenin gövdesine ekle.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Birleştirilmiş içeriği zaten manuel olarak eklediğimizden,
            // Bu olaya "Metin" özelliği aracılığıyla içerik döndürerek yanıt vermemize gerek kalmayacak.
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Hiçbir şey yapmayın.
    }
}
```

### Ayrıca bakınız

* class [FieldMergingArgsBase](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)

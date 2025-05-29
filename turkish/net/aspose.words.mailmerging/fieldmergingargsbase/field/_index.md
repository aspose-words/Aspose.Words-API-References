---
title: FieldMergingArgsBase.Field
linktitle: Field
articleTitle: Field
second_title: .NET için Aspose.Words
description: Mevcut birleştirme alanı nesnesine zahmetsizce erişmek için FieldMergingArgsBase Field özelliğini keşfedin. Veri birleştirme verimliliğinizi bugün artırın!
type: docs
weight: 30
url: /tr/net/aspose.words.mailmerging/fieldmergingargsbase/field/
---
## FieldMergingArgsBase.Field property

Geçerli birleştirme alanını temsil eden nesneyi alır.

```csharp
public FieldMergeField Field { get; }
```

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

* class [FieldMergeField](../../../aspose.words.fields/fieldmergefield/)
* class [FieldMergingArgsBase](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)

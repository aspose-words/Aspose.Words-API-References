---
title: FieldAsk.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: .NET için Aspose.Words
description: Yer imlerinizi kolayca yönetmek ve özelleştirmek için FieldAsk BookmarkName özelliğini keşfedin. Kusursuz gezinmeyle kullanıcı deneyiminizi geliştirin!
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldask/bookmarkname/
---
## FieldAsk.BookmarkName property

Yer iminin adını alır veya ayarlar.

```csharp
public string BookmarkName { get; set; }
```

## Örnekler

ASK alanının nasıl oluşturulacağını ve özelliklerinin nasıl ayarlanacağını gösterir.

```csharp
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // ASK alanımıza verilecek cevabın yer alacağı bir alan yerleştiriyoruz.
    FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    fieldRef.BookmarkName = "MyAskField";
    builder.Writeln();

    Assert.AreEqual(" REF  MyAskField", fieldRef.GetFieldCode());

    // ASK alanını ekleyin ve özelliklerini düzenleyerek yer imi adına göre REF alanımıza başvuralım.
    FieldAsk fieldAsk = (FieldAsk)builder.InsertField(FieldType.FieldAsk, true);
    fieldAsk.BookmarkName = "MyAskField";
    fieldAsk.PromptText = "Please provide a response for this ASK field";
    fieldAsk.DefaultResponse = "Response from within the field.";
    fieldAsk.PromptOnceOnMailMerge = true;
    builder.Writeln();

    Assert.AreEqual(
        " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
        fieldAsk.GetFieldCode());

    // ASK alanları, bir posta birleştirme sırasında ilgili REF alanlarına varsayılan yanıtı uygular.
    DataTable table = new DataTable("My Table");
    table.Columns.Add("Column 1");
    table.Rows.Add("Row 1");
    table.Rows.Add("Row 2");

    FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    fieldMergeField.FieldName = "Column 1";

    // ASK alanlarımızdaki varsayılan yanıtı özel bir istem yanıtlayıcısıyla değiştirebilir veya geçersiz kılabiliriz.
    // posta birleştirme sırasında gerçekleşecektir.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");
}

/// <summary>
/// Bir posta birleştirme sırasında ASK alanının varsayılan yanıtına metin ekler.
/// </summary>
private class MyPromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response from MyPromptRespondent. " + defaultResponse;
    }
}
```

### Ayrıca bakınız

* class [FieldAsk](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

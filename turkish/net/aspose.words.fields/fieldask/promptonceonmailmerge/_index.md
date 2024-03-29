---
title: FieldAsk.PromptOnceOnMailMerge
linktitle: PromptOnceOnMailMerge
articleTitle: PromptOnceOnMailMerge
second_title: Aspose.Words for .NET
description: FieldAsk PromptOnceOnMailMerge mülk. Adresmektup birleştirme işlemi başına kullanıcı yanıtının bir kez alınması gerekip gerekmediğini alır veya ayarlar C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldask/promptonceonmailmerge/
---
## FieldAsk.PromptOnceOnMailMerge property

Adres-mektup birleştirme işlemi başına kullanıcı yanıtının bir kez alınması gerekip gerekmediğini alır veya ayarlar.

```csharp
public bool PromptOnceOnMailMerge { get; set; }
```

## Örnekler

ASK alanının nasıl oluşturulacağını ve özelliklerinin nasıl ayarlanacağını gösterir.

```csharp
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // ASK alanımıza verilecek yanıtın yerleştirileceği alanı yerleştirin.
    FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    fieldRef.BookmarkName = "MyAskField";
    builder.Writeln();

    Assert.AreEqual(" REF  MyAskField", fieldRef.GetFieldCode());

    // ASK alanını ekleyin ve REF alanımıza yer işareti adıyla referans verecek şekilde özelliklerini düzenleyin.
    FieldAsk fieldAsk = (FieldAsk)builder.InsertField(FieldType.FieldAsk, true);
    fieldAsk.BookmarkName = "MyAskField";
    fieldAsk.PromptText = "Please provide a response for this ASK field";
    fieldAsk.DefaultResponse = "Response from within the field.";
    fieldAsk.PromptOnceOnMailMerge = true;
    builder.Writeln();

    Assert.AreEqual(
        " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
        fieldAsk.GetFieldCode());

    // ASK alanları, adres-mektup birleştirme sırasında ilgili REF alanlarına varsayılan yanıtı uygular.
    DataTable table = new DataTable("My Table");
    table.Columns.Add("Column 1");
    table.Rows.Add("Row 1");
    table.Rows.Add("Row 2");

    FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    fieldMergeField.FieldName = "Column 1";

    // Özel bir istem yanıtlayıcı ile ASK alanlarımızdaki varsayılan yanıtı değiştirebilir veya geçersiz kılabiliriz,
    // adres-mektup birleştirme sırasında gerçekleşecek.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");
}

/// <summary>
/// Adres-mektup birleştirme sırasında ASK alanının varsayılan yanıtının başına metin ekler.
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

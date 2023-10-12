---
title: MailMerge.MergeWholeDocument
second_title: Aspose.Words for .NET API Referansı
description: MailMerge mülk. Bölgelerle adresmektup birleştirme yürütülürken belgenin tamamındaki alanların güncellenip güncellenmediğini gösteren bir değer alır veya ayarlar.
type: docs
weight: 70
url: /tr/net/aspose.words.mailmerging/mailmerge/mergewholedocument/
---
## MailMerge.MergeWholeDocument property

Bölgelerle adres-mektup birleştirme yürütülürken belgenin tamamındaki alanların güncellenip güncellenmediğini gösteren bir değer alır veya ayarlar.

```csharp
public bool MergeWholeDocument { get; set; }
```

### Notlar

Varsayılan değer:`YANLIŞ` .

### Örnekler

Bölgelerle adres-mektup birleştirmeler ve alan güncelleme arasındaki ilişkiyi gösterir.

```csharp
public void MergeWholeDocument(bool mergeWholeDocument)
{
    Document doc = CreateSourceDocMergeWholeDocument();
    DataTable dataTable = CreateSourceTableMergeWholeDocument();

    // "MergeWholeDocument" bayrağını "true" olarak ayarlarsak,
    // bölgelerle adres-mektup birleştirme belgedeki her alanı güncelleyecektir.
    // "MergeWholeDocument" bayrağını "false" olarak ayarlarsak adres-mektup birleştirme yalnızca alanları günceller
    // adı veri kaynağı tablosunun adıyla eşleşen adres-mektup birleştirme bölgesi içinde.
    doc.MailMerge.MergeWholeDocument = mergeWholeDocument;
    doc.MailMerge.ExecuteWithRegions(dataTable);

    // Adres-mektup birleştirme yalnızca adres-mektup birleştirme bölgesinin dışındaki QUOTE alanını güncelleyecektir
    // "MergeWholeDocument" bayrağını "true" olarak ayarlarsak.
    doc.Save(ArtifactsDir + "MailMerge.MergeWholeDocument.docx");

    Assert.True(doc.GetText().Contains("This QUOTE field is inside the \"MyTable\" merge region."));
    Assert.AreEqual(mergeWholeDocument, 
        doc.GetText().Contains("This QUOTE field is outside of the \"MyTable\" merge region."));
}

/// <summary>
/// "Tablom" adlı bir veri kaynağına ait adres-mektup birleştirme bölgesine sahip bir belge oluşturun.
/// Bu bölgenin içine bir QUOTE alanı ve dışına bir tane daha ekleyin.
/// </summary>
private static Document CreateSourceDocMergeWholeDocument()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
    field.Text = "This QUOTE field is outside of the \"MyTable\" merge region.";

    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD TableStart:MyTable");

    field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
    field.Text = "This QUOTE field is inside the \"MyTable\" merge region.";
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD MyColumn");
    builder.InsertField(" MERGEFIELD TableEnd:MyTable");

    return doc;
}

/// <summary>
/// Adres-mektup birleştirmede kullanılacak bir veri tablosu oluşturun.
/// </summary>
private static DataTable CreateSourceTableMergeWholeDocument()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("MyColumn");
    dataTable.Rows.Add(new object[] { "MyValue" });

    return dataTable;
}
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge/)
* toplantı [Aspose.Words](../../../)



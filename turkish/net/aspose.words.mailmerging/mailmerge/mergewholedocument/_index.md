---
title: MailMerge.MergeWholeDocument
linktitle: MergeWholeDocument
articleTitle: MergeWholeDocument
second_title: .NET için Aspose.Words
description: MailMerge MergeWholeDocument özelliğinin, bölge tabanlı bir posta birleştirme işlemi sırasında tüm alanları nasıl güncelleyerek belgelerinizdeki verimliliği ve doğruluğu artırdığını keşfedin.
type: docs
weight: 70
url: /tr/net/aspose.words.mailmerging/mailmerge/mergewholedocument/
---
## MailMerge.MergeWholeDocument property

Bölgelerle bir posta birleştirme işlemi yürütülürken tüm belgedeki alanların güncellenip güncellenmeyeceğini belirten bir değer alır veya ayarlar.

```csharp
public bool MergeWholeDocument { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ` .

## Örnekler

Bölgelerle posta birleştirmeleri ve alan güncellemeleri arasındaki ilişkiyi gösterir.

```csharp
public void MergeWholeDocument(bool mergeWholeDocument)
{
    Document doc = CreateSourceDocMergeWholeDocument();
    DataTable dataTable = CreateSourceTableMergeWholeDocument();

    // "MergeWholeDocument" bayrağını "true" olarak ayarlarsak,
    // Bölgelerle yapılan posta birleştirme işlemi belgedeki her alanı güncelleyecektir.
    // "MergeWholeDocument" bayrağını "false" olarak ayarlarsak, posta birleştirme yalnızca alanları günceller
    // adı veri kaynağı tablosunun adıyla eşleşen posta birleştirme bölgesi içinde.
    doc.MailMerge.MergeWholeDocument = mergeWholeDocument;
    doc.MailMerge.ExecuteWithRegions(dataTable);

    // Posta birleştirme yalnızca posta birleştirme bölgesinin dışında QUOTE alanını güncelleyecektir
    // "MergeWholeDocument" bayrağını "true" olarak ayarlarsak.
    doc.Save(ArtifactsDir + "MailMerge.MergeWholeDocument.docx");

    Assert.True(doc.GetText().Contains("This QUOTE field is inside the \"MyTable\" merge region."));
    Assert.AreEqual(mergeWholeDocument, 
        doc.GetText().Contains("This QUOTE field is outside of the \"MyTable\" merge region."));
}

/// <summary>
/// "MyTable" adlı bir veri kaynağına ait bir posta birleştirme bölgesi içeren bir belge oluşturun.
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
/// Bir posta birleştirme işleminde kullanılacak veri tablosunu oluşturun.
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
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)

---
title: FieldAutoNumLgl.SeparatorCharacter
linktitle: SeparatorCharacter
articleTitle: SeparatorCharacter
second_title: Aspose.Words for .NET
description: FieldAutoNumLgl SeparatorCharacter mülk. Kullanılacak ayırıcı karakteri alır veya ayarlar C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldautonumlgl/separatorcharacter/
---
## FieldAutoNumLgl.SeparatorCharacter property

Kullanılacak ayırıcı karakteri alır veya ayarlar.

```csharp
public string SeparatorCharacter { get; set; }
```

## Örnekler

AUTONUMLGL alanlarını kullanarak bir belgenin nasıl düzenleneceğini gösterir.

```csharp
public void FieldAutoNumLgl()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    const string fillerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
                              "\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ";

    // AUTONUMLGL alanları, geçerli başlık düzeyi dahilinde her AUTONUMLGL alanında artan bir sayı görüntüler.
    // Bu alanlar her başlık seviyesi için ayrı bir sayım tutar,
     // ve her alan aynı zamanda kendisinin altındaki tüm başlık seviyeleri için AUTONUMLGL alan sayımlarını da görüntüler.
    // Herhangi bir yön düzeyine ilişkin sayıyı değiştirmek, o düzeyin üzerindeki tüm düzeylere ilişkin sayıları 1'e sıfırlar.
    // Bu, belgemizi bir taslak liste biçiminde düzenlememizi sağlar.
    // Bu, "1"i görüntüleyen, 1 başlık seviyesindeki ilk AUTONUMLGL alanıdır. belgede.
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // Bu, 1 başlık düzeyindeki ikinci AUTONUMLGL alanıdır, dolayısıyla "2." görüntülenecektir.
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // Bu, 2 başlık seviyesindeki ilk AUTONUMLGL alanıdır,
    // ve altındaki başlık düzeyi için AUTONUMLGL sayısı "2"dir, dolayısıyla "2.1." görüntülenecektir.
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

     // Bu, 3 başlık düzeyindeki ilk AUTONUMLGL alanıdır.
    // Yukarıdaki alanla aynı şekilde çalıştığında "2.1.1." görüntülenecektir.
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // Bu alan 2 başlık seviyesindedir ve ilgili AUTONUMLGL sayısı 2'dir, dolayısıyla alan "2.2." gösterecektir.
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // Bunun altındaki bir yön seviyesi için AUTONUMLGL sayısını artırıyoruz
    // bu alanda "2.2.1." görüntülenecek şekilde bu seviyenin sayımı sıfırlandı.
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal))
    {
        // Sayının hemen ardından alan sonucunda görünen ayırıcı karakter,
        // varsayılan olarak noktadır. Bu özelliği null bırakırsak,
        // son AUTONUMLGL alanımız "2.2.1" gösterecektir. belgede.
        Assert.IsNull(field.SeparatorCharacter);

        // Özel bir ayırıcı karakter ayarlama ve sondaki noktayı kaldırma
        // bu alanın görünümünü "2.2.1"den değiştirecek. "2:2:1"e değiştirin.
        // Bunu oluşturduğumuz tüm alanlara uygulayacağız.
        field.SeparatorCharacter = ":";
        field.RemoveTrailingPeriod = true;
        Assert.AreEqual(" AUTONUMLGL  \\s : \\e", field.GetFieldCode());
    }

    doc.Save(ArtifactsDir + "Field.AUTONUMLGL.docx");
}

/// <summary>
/// AUTONUMLGL alanıyla numaralandırılmış bir yan tümce eklemek için belge oluşturucuyu kullanır.
/// </summary>
private static void InsertNumberedClause(DocumentBuilder builder, string heading, string contents, StyleIdentifier headingStyle)
{
    builder.InsertField(FieldType.FieldAutoNumLegal, true);
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = headingStyle;
    builder.Writeln(heading);

    // Bu metin, üstündeki otomatik numara yasal alanına ait olacaktır.
    // Microsoft Word'de ilgili AUTONUMLGL alanının yanındaki oka tıkladığımızda çökecektir.
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### Ayrıca bakınız

* class [FieldAutoNumLgl](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

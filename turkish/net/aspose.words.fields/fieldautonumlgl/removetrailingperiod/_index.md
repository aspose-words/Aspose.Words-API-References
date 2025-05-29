---
title: FieldAutoNumLgl.RemoveTrailingPeriod
linktitle: RemoveTrailingPeriod
articleTitle: RemoveTrailingPeriod
second_title: .NET için Aspose.Words
description: Sayı görüntüsünü özelleştirmek için FieldAutoNumLgl'nin RemoveTrailingPeriod özelliğini yönetin; daha temiz, profesyonel biçimlendirme için sondaki noktaları ortadan kaldırın.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldautonumlgl/removetrailingperiod/
---
## FieldAutoNumLgl.RemoveTrailingPeriod property

Sayının sonunda nokta olmadan gösterilip gösterilmeyeceğini alır veya ayarlar.

```csharp
public bool RemoveTrailingPeriod { get; set; }
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

    // AUTONUMLGL alanları, geçerli başlık düzeyindeki her AUTONUMLGL alanında artan bir sayı görüntüler.
    // Bu alanlar her başlık düzeyi için ayrı bir sayım tutar,
     // ve her alan ayrıca kendi altındaki tüm başlık düzeyleri için AUTONUMLGL alan sayılarını görüntüler.
    // Herhangi bir başlık düzeyi için sayımı değiştirmek, o düzeyin üzerindeki tüm düzeylerin sayımını 1'e sıfırlar.
    // Bu, belgemizi bir ana hat listesi şeklinde düzenlememizi sağlar.
    // Bu, başlık düzeyi 1 olan ilk AUTONUMLGL alanıdır ve belgede "1." görüntüler.
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // Bu, başlık düzeyi 1 olan ikinci AUTONUMLGL alanıdır, bu nedenle "2." görüntülenecektir.
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // Bu, 2 başlık düzeyindeki ilk AUTONUMLGL alanıdır.
    // ve altındaki başlık seviyesi için AUTONUMLGL sayısı "2" olduğundan "2.1." görüntülenecektir.
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

     // Bu, başlık düzeyi 3 olan ilk AUTONUMLGL alanıdır.
    // Yukarıdaki alanla aynı şekilde çalışarak "2.1.1." görüntülenecektir.
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // Bu alan 2 başlık düzeyindedir ve ilgili AUTONUMLGL sayısı 2'dir, bu nedenle alan "2.2." gösterecektir.
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // Bu seviyenin altındaki bir başlık seviyesi için AUTONUMLGL sayısının artırılması
    // Bu seviye için sayımı sıfırladı, böylece bu alan "2.2.1." olarak görüntülenecek.
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal).ToList())
    {
        // Alan sonucu alanında sayıdan hemen sonra görünen ayırıcı karakter,
        // varsayılan olarak tam bir noktadır. Bu özelliği boş bırakırsak,
        // Son AUTONUMLGL alanımız belgede "2.2.1." görüntüleyecektir.
        Assert.IsNull(field.SeparatorCharacter);

        // Özel bir ayırıcı karakter ayarlama ve son noktayı kaldırma
        // Bu alanın görünümünü "2.2.1."den "2:2:1"e değiştirecektir.
        // Bunu oluşturduğumuz tüm alanlara uygulayacağız.
        field.SeparatorCharacter = ":";
        field.RemoveTrailingPeriod = true;
        Assert.AreEqual(" AUTONUMLGL  \\s : \\e", field.GetFieldCode());
    }

    doc.Save(ArtifactsDir + "Field.AUTONUMLGL.docx");
}

/// <summary>
/// Bir AUTONUMLGL alanıyla numaralandırılmış bir madde eklemek için bir belge oluşturucu kullanır.
/// </summary>
private static void InsertNumberedClause(DocumentBuilder builder, string heading, string contents, StyleIdentifier headingStyle)
{
    builder.InsertField(FieldType.FieldAutoNumLegal, true);
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = headingStyle;
    builder.Writeln(heading);

    // Bu metin, üstündeki auto num legal alanına ait olacaktır.
    // Microsoft Word'de ilgili AUTONUMLGL alanının yanındaki oka tıkladığımızda kapanacaktır.
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### Ayrıca bakınız

* class [FieldAutoNumLgl](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

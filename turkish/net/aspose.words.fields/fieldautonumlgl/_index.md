---
title: FieldAutoNumLgl Class
linktitle: FieldAutoNumLgl
articleTitle: FieldAutoNumLgl
second_title: .NET için Aspose.Words
description: AUTONUMLGL alanlarının sorunsuz uygulanması, belge otomasyonunun ve biçimlendirmesinin geliştirilmesi için Aspose.Words.Fields.FieldAutoNumLgl sınıfını keşfedin.
type: docs
weight: 2000
url: /tr/net/aspose.words.fields/fieldautonumlgl/
---
## FieldAutoNumLgl class

AUTONUMLGL alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldAutoNumLgl : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldAutoNumLgl](fieldautonumlgl/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [RemoveTrailingPeriod](../../aspose.words.fields/fieldautonumlgl/removetrailingperiod/) { get; set; } | Sayının sonunda nokta olmadan gösterilip gösterilmeyeceğini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [SeparatorCharacter](../../aspose.words.fields/fieldautonumlgl/separatorcharacter/) { get; set; } | Kullanılacak ayırıcı karakteri alır veya ayarlar. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son alt 'siyse, üst paragrafını döndürür. Alan zaten kaldırılmışsa, şunu döndürür`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alan bağlantısını kaldırma işlemini gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |

## Notlar

Yasal formatta otomatik bir sayı ekler.

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

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)

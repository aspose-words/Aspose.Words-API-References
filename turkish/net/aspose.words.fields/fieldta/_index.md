---
title: Class FieldTA
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.FieldTA sınıf. TA alanını uygular.
type: docs
weight: 2320
url: /tr/net/aspose.words.fields/fieldta/
---
## FieldTA class

TA alanını uygular.

```csharp
public class FieldTA : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldTA](fieldta/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [EntryCategory](../../aspose.words.fields/fieldta/entrycategory/) { get; set; } | kategorilerinin sırasına karşılık gelen bir sayı olan integral giriş kategorisini alır veya ayarlar. |
| [Format](../../aspose.words.fields/field/format/) { get; } | [`FieldFormat`](../fieldformat/) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [IsBold](../../aspose.words.fields/fieldta/isbold/) { get; set; } | Girdi için sayfa numarasına kalın biçimlendirme uygulanıp uygulanmayacağını belirler. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsItalic](../../aspose.words.fields/fieldta/isitalic/) { get; set; } | Girdi için sayfa numarasına italik biçimlendirme uygulanıp uygulanmayacağını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [LongCitation](../../aspose.words.fields/fieldta/longcitation/) { get; set; } | Girdi için uzun alıntıyı alır veya ayarlar. |
| [PageRangeBookmarkName](../../aspose.words.fields/fieldta/pagerangebookmarkname/) { get; set; } | Girdinin sayfa numarası olarak eklenen bir sayfa aralığını işaretleyen yer iminin adını alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [ShortCitation](../../aspose.words.fields/fieldta/shortcitation/) { get; set; } | Giriş için kısa alıntıyı alır veya ayarlar. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alandan hemen sonra bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğu ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa, döner **hükümsüz** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Bağlantıyı kaldır alanını gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

### Notlar

Bir TOA alanı tarafından kullanılan bir otorite tablosu girişi için metin ve sayfa numarasını tanımlar.

### Örnekler

TOA ve TA alanlarını kullanarak bir yetki tablosunun nasıl oluşturulacağını ve özelleştirileceğini gösterir.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Belgedeki her bir TA alanı için bir giriş oluşturacak bir TOA alanı ekleyin,
    // her giriş için uzun alıntılar ve sayfa numaraları gösteriliyor.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // Tablomuz için giriş kategorisini ayarlayın. Bu TOA artık yalnızca TA alanlarını içerecek
    // EntryCategory özelliğinde eşleşen bir değere sahip olan.
    fieldToa.EntryCategory = "1";

    // Ayrıca, Dizin 1'deki Yetkiler Tablosu kategorisi "Vakalar",
    // bu değişkeni true olarak ayarlarsak tablomuzun başlığı olarak görünecektir.
    fieldToa.UseHeading = true;

    // TOA sınırları içinde olması gereken bir yer imi adlandırarak TA alanlarını daha fazla filtreleyebiliriz.
    fieldToa.BookmarkName = "MyBookmark";

    // Varsayılan olarak, TA alanının alıntısı arasında sayfa çapında noktalı bir sekme görünür
    // ve sayfa numarası. Bu özelliğe koyduğumuz herhangi bir metinle değiştirebiliriz.
    // Bir sekme karakteri eklemek orijinal sekmeyi koruyacaktır.
    fieldToa.EntrySeparator = " \t p.";

    // Aynı uzun alıntıyı paylaşan birden fazla TA girişimiz varsa,
    // ilgili tüm sayfa numaraları bir satırda görünecektir.
    // Sayfa numaralarını ayıracak bir dize belirtmek için bu özelliği kullanabiliriz.
    fieldToa.PageNumberListSeparator = " & p. ";

    // Tablomuzun "passim" kelimesini göstermesini sağlamak için bunu true olarak ayarlayabiliriz.
    // bir satırda beş veya daha fazla sayfa numarası varsa.
    fieldToa.UsePassim = true;

    // Bir TA alanı bir dizi sayfaya başvurabilir.
    // Bu tür aralıklar için başlangıç ve bitiş sayfa numaraları arasında görünecek bir dize belirtebiliriz.
    fieldToa.PageRangeSeparator = " to ";

    // TA alanlarındaki format tablomuza taşınacaktır.
    // RemoveEntryFormatting bayrağını ayarlayarak bunu devre dışı bırakabiliriz.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Bu TA alanı, dışarıda olduğu için TOA'da bir giriş olarak görünmeyecektir.
    // TOA'nın BookmarkName özelliğinin belirttiği yer iminin sınırları.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // Bu TA alanı yer iminin içindedir,
    // ancak giriş kategorisi tablonunkiyle eşleşmiyor, bu nedenle TA alanı onu içermeyecek.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // Bu giriş tabloda görünecektir.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // Bir TOA tablosu kısa alıntıları göstermez,
    // ancak bunları birden çok TA alanının başvurduğu hacimli kaynak adlarına başvurmak için bir kısayol olarak kullanabiliriz.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // Aşağıdaki özellikleri kullanarak sayfa numarasını kalın/italik yapacak şekilde biçimlendirebiliriz.
    // Tablomuzu biçimlendirmeyi yok sayacak şekilde ayarlarsak bu etkileri görmeye devam edeceğiz.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // TA alanlarını, TOA girişlerini bir yer iminin yayıldığı bir dizi sayfaya atıfta bulunacak şekilde yapılandırabiliriz.
    // Tablomuzdaki bir satırı paylaşmak için bu girişin yukarıdaki ile aynı kaynağa atıfta bulunduğunu unutmayın.
    // Bu satır, yukarıdaki girişin sayfa numarasına ve bu girişin sayfa aralığına sahip olacaktır,
    // tablonun sayfa listesi ve sayfa numaraları arasında sayfa numarası aralığı ayırıcıları ile.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // Tablomuzun "Passim" özelliğini etkinleştirmişsek, aynı kaynakla 5 veya daha fazla TA girişi olması onu çağıracaktır.
    for (int i = 0; i < 5; i++)
    {
        InsertToaEntry(builder, "1", "Source 4");
    }

    builder.EndBookmark("MyBookmark");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOA.TA.docx");

private static FieldTA InsertToaEntry(DocumentBuilder builder, string entryCategory, string longCitation)
{
    FieldTA field = (FieldTA)builder.InsertField(FieldType.FieldTOAEntry, false);
    field.EntryCategory = entryCategory;
    field.LongCitation = longCitation;

    builder.InsertBreak(BreakType.PageBreak);

    return field;
}
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)



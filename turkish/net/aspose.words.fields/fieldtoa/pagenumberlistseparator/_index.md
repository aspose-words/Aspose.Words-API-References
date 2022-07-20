---
title: PageNumberListSeparator
second_title: Aspose.Words for .NET API Referansı
description: Bir sayfa numarası listesindeki iki sayfa numarasını ayırmak için kullanılan karakter dizisini alır veya ayarlar.
type: docs
weight: 50
url: /tr/net/aspose.words.fields/fieldtoa/pagenumberlistseparator/
---
## FieldToa.PageNumberListSeparator property

Bir sayfa numarası listesindeki iki sayfa numarasını ayırmak için kullanılan karakter dizisini alır veya ayarlar.

```csharp
public string PageNumberListSeparator { get; set; }
```

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

* class [FieldToa](../../fieldtoa)
* ad alanı [Aspose.Words.Fields](../../fieldtoa)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

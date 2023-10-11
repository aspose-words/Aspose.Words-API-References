---
title: FieldToa.RemoveEntryFormatting
second_title: Aspose.Words for .NET API Referansı
description: FieldToa mülk. Belgedeki giriş metninin formatının yetki tablosundaki girişinden kaldırılıp kaldırılmayacağını alır veya ayarlar.
type: docs
weight: 70
url: /tr/net/aspose.words.fields/fieldtoa/removeentryformatting/
---
## FieldToa.RemoveEntryFormatting property

Belgedeki giriş metninin formatının yetki tablosundaki girişinden kaldırılıp kaldırılmayacağını alır veya ayarlar.

```csharp
public bool RemoveEntryFormatting { get; set; }
```

### Örnekler

TOA ve TA alanlarını kullanarak bir yetki tablosunun nasıl oluşturulacağını ve özelleştirileceğini gösterir.

```csharp
public void FieldTOA()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Belgedeki her TA alanı için bir giriş oluşturacak bir TOA alanı ekleyin,
    // her giriş için uzun alıntılar ve sayfa numaraları görüntüleniyor.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // Tablomuz için giriş kategorisini ayarlayın. Bu TOA artık yalnızca TA alanlarını içerecektir
    // EntryCategory özelliğinde eşleşen bir değere sahip olanlar.
    fieldToa.EntryCategory = "1";

    // Ayrıca indeks 1'deki Yetki Tablosu kategorisi "Vakalar"dır,
    // bu değişkeni true olarak ayarlarsak tablomuzun başlığı olarak görünecektir.
    fieldToa.UseHeading = true;

    // TOA sınırları içinde olmaları gereken bir yer imini adlandırarak TA alanlarını daha da filtreleyebiliriz.
    fieldToa.BookmarkName = "MyBookmark";

    // Varsayılan olarak, TA alanının alıntısı arasında sayfa çapında noktalı bir sekme görünür
    // ve sayfa numarası. Bunu, bu özelliğe koyduğumuz herhangi bir metinle değiştirebiliriz.
    // Bir sekme karakteri eklemek orijinal sekmeyi koruyacaktır.
    fieldToa.EntrySeparator = " \t p.";

    // Aynı uzun alıntıyı paylaşan birden fazla TA girişimiz varsa,
    // ilgili tüm sayfa numaraları tek satırda görünecektir.
    // Sayfa numaralarını ayıracak bir dize belirtmek için bu özelliği kullanabiliriz.
    fieldToa.PageNumberListSeparator = " & p. ";

    // Tablomuzun "passim" kelimesini göstermesini sağlamak için bunu true olarak ayarlayabiliriz
    // bir satırda beş veya daha fazla sayfa numarası varsa.
    fieldToa.UsePassim = true;

    // Bir TA alanı çeşitli sayfalara başvurabilir.
    // Bu tür aralıklar için başlangıç ve bitiş sayfa numaraları arasında görünecek bir dizeyi burada belirtebiliriz.
    fieldToa.PageRangeSeparator = " to ";

    // TA alanlarındaki format tablomuza taşınacaktır.
    // RemoveEntryFormatting bayrağını ayarlayarak bunu devre dışı bırakabiliriz.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Bu TA alanı TOA'nın dışında olduğundan giriş olarak görünmeyecektir.
    // TOA'nın BookmarkName özelliğinin belirttiği yer iminin sınırları.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // Bu TA alanı yer iminin içindedir,
    // ancak giriş kategorisi tablonunkiyle eşleşmediğinden TA alanı onu içermeyecektir.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // Bu giriş tabloda görünecektir.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // TOA tablosu kısa alıntıları göstermez,
    // ancak bunları birden fazla TA alanının referans verdiği büyük kaynak adlarına atıfta bulunmak için kısa yol olarak kullanabiliriz.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // Aşağıdaki özellikleri kullanarak sayfa numarasını kalın/italik yapacak şekilde biçimlendirebiliriz.
    // Tablomuzu biçimlendirmeyi göz ardı edecek şekilde ayarlarsak yine de bu efektleri göreceğiz.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // TA alanlarını, TOA girişlerinin bir yer iminin yayıldığı bir dizi sayfaya başvurmasını sağlayacak şekilde yapılandırabiliriz.
    // Tablomuzdaki bir satırı paylaşmak için bu girdinin yukarıdakiyle aynı kaynağa başvurduğunu unutmayın.
    // Bu satırda yukarıdaki girişin sayfa numarası ve bu girişin sayfa aralığı yer alacaktır,
    // tablonun sayfa listesi ve sayfa numaraları arasındaki sayfa numarası aralığı ayırıcıları ile.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // Tablomuzun "Passim" özelliğini etkinleştirmişsek, aynı kaynaktan 5 veya daha fazla TA girişi olması onu çağıracaktır.
    for (int i = 0; i < 5; i++)
    {
        InsertToaEntry(builder, "1", "Source 4");
    }

    builder.EndBookmark("MyBookmark");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOA.TA.docx");
}

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

* class [FieldToa](../)
* ad alanı [Aspose.Words.Fields](../../fieldtoa/)
* toplantı [Aspose.Words](../../../)



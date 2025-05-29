---
title: FieldToa.RemoveEntryFormatting
linktitle: RemoveEntryFormatting
articleTitle: RemoveEntryFormatting
second_title: .NET için Aspose.Words
description: Belgenizdeki giriş metni biçimlendirmesini FieldToa'nın RemoveEntryFormatting özelliğiyle kontrol edin. Kaynak tablonuzu zahmetsizce geliştirin!
type: docs
weight: 70
url: /tr/net/aspose.words.fields/fieldtoa/removeentryformatting/
---
## FieldToa.RemoveEntryFormatting property

Yetkililer tablosundaki girişinden belgedeki giriş metninin biçimlendirmesinin kaldırılıp kaldırılmayacağını alır veya ayarlar.

```csharp
public bool RemoveEntryFormatting { get; set; }
```

## Örnekler

TOA ve TA alanlarını kullanarak bir yetki tablosunun nasıl oluşturulacağını ve özelleştirileceğini gösterir.

```csharp
public void FieldTOA()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Belgedeki her TA alanı için bir giriş oluşturacak bir TOA alanı ekleyin,
    // her girdi için uzun alıntılar ve sayfa numaraları görüntüleniyor.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // Tablomuz için giriş kategorisini ayarlayın. Bu TOA artık yalnızca TA alanlarını içerecektir
    // EntryCategory özelliğinde eşleşen bir değere sahip olanlar.
    fieldToa.EntryCategory = "1";

    // Ayrıca, 1. indeksteki Yetki Tablosu kategorisi "Vakalar"dır,
    // bu değişkeni true olarak ayarlarsak tablomuzun başlığı olarak görünecektir.
    fieldToa.UseHeading = true;

    // TA alanlarını, TOA sınırları içerisinde olması gereken bir yer imi adlandırarak daha fazla filtreleyebiliriz.
    fieldToa.BookmarkName = "MyBookmark";

    // Varsayılan olarak, TA alanının atıfları arasında noktalı çizgi şeklinde sayfa çapında bir sekme görünür
    // ve sayfa numarası. Bunu bu özelliğe koyduğumuz herhangi bir metinle değiştirebiliriz.
    // Bir sekme karakteri eklemek orijinal sekmeyi koruyacaktır.
    fieldToa.EntrySeparator = " \t p.";

    // Aynı uzun atıfı paylaşan birden fazla TA girişimiz varsa,
    // tüm sayfa numaraları tek bir satırda gösterilecektir.
    // Bu özelliği, sayfa numaralarını ayıracak bir dize belirtmek için kullanabiliriz.
    fieldToa.PageNumberListSeparator = " & p. ";

    // Tablomuzun "passim" kelimesini görüntülemesini sağlamak için bunu true olarak ayarlayabiliriz
    // bir satırda beş veya daha fazla sayfa numarası varsa.
    fieldToa.UsePassim = true;

    // Bir TA alanı bir dizi sayfaya atıfta bulunabilir.
    // Bu tür aralıklar için başlangıç ve bitiş sayfa numaraları arasında görünecek bir stringi burada belirtebiliriz.
    fieldToa.PageRangeSeparator = " to ";

    // TA alanlarındaki format tablomuza aktarılacak.
    // Bunu RemoveEntryFormatting bayrağını ayarlayarak devre dışı bırakabiliriz.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Bu TA alanı TOA'da bir giriş olarak görünmeyecektir çünkü dışarıdadır
    // TOA'nın BookmarkName özelliğinin belirttiği yer iminin sınırları.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // Bu TA alanı yer iminin içindedir,
    // ancak giriş kategorisi tablonun kategorisiyle uyuşmuyor, bu nedenle TA alanı bunu içermeyecektir.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // Bu giriş tabloda görünecektir.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // Bir TOA tablosu kısa alıntıları görüntülemez,
    // ancak bunları, birden fazla TA alanının başvurduğu hacimli kaynak adlarına atıfta bulunmak için bir kısaltma olarak kullanabiliriz.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // Aşağıdaki özellikleri kullanarak sayfa numarasını kalın/italik hale getirebiliriz.
    // Tablomuzu biçimlendirmeyi göz ardı edecek şekilde ayarlarsak bu etkileri yine göreceğiz.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // TA alanlarını, yer iminin kapsadığı sayfa aralığına atıfta bulunacak şekilde TOA girişleri alacak şekilde yapılandırabiliriz.
    // Bu girdinin, tablomuzda bir satırı paylaşmak için yukarıdaki girdiyle aynı kaynağa başvurduğunu unutmayın.
    // Bu satır, yukarıdaki girdinin sayfa numarasını ve bu girdinin sayfa aralığını içerecektir.
    // sayfa numaraları arasında tablonun sayfa listesi ve sayfa numarası aralığı ayırıcıları bulunur.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // Eğer tablomuzun "Passim" özelliğini aktifleştirdiysek, aynı kaynaktan 5 veya daha fazla TA girişi olması durumunda bu özellik çağrılacaktır.
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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

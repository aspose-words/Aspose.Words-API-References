---
title: FieldToa Class
linktitle: FieldToa
articleTitle: FieldToa
second_title: .NET için Aspose.Words
description: Kusursuz TOA alan uygulaması için Aspose.Words.Fields.FieldToa sınıfını keşfedin. Belge işlemenizi bugün güçlü özellikler ile geliştirin!
type: docs
weight: 2930
url: /tr/net/aspose.words.fields/fieldtoa/
---
## FieldToa class

TOA alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldToa : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldToa](fieldtoa/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoa/bookmarkname/) { get; set; } | Tabloyu oluşturmak için kullanılan belge bölümünü işaretleyen yer iminin adını alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [EntryCategory](../../aspose.words.fields/fieldtoa/entrycategory/) { get; set; } | Tabloda yer alan girdiler için integral kategorisini alır veya ayarlar. |
| [EntrySeparator](../../aspose.words.fields/fieldtoa/entryseparator/) { get; set; } | Yetkili bir tablo girişini ve sayfa numarasını ayırmak için kullanılan karakter dizisini alır veya ayarlar. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldtoa/pagenumberlistseparator/) { get; set; } | Bir sayfa numarası listesinde iki sayfa numarasını ayırmak için kullanılan karakter dizisini alır veya ayarlar. |
| [PageRangeSeparator](../../aspose.words.fields/fieldtoa/pagerangeseparator/) { get; set; } | Bir sayfa aralığının başlangıcını ve sonunu ayırmak için kullanılan karakter dizisini alır veya ayarlar. |
| [RemoveEntryFormatting](../../aspose.words.fields/fieldtoa/removeentryformatting/) { get; set; } | Yetkililer tablosundaki girişinden belgedeki giriş metninin biçimlendirmesinin kaldırılıp kaldırılmayacağını alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [SequenceName](../../aspose.words.fields/fieldtoa/sequencename/) { get; set; } | Sayfa numarasına dahil olan bir dizinin adını alır veya ayarlar. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoa/sequenceseparator/) { get; set; } | Sıra numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter dizisini alır veya ayarlar. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |
| [UseHeading](../../aspose.words.fields/fieldtoa/useheading/) { get; set; } | Yetkililer tablosundaki girdiler için kategori başlığının eklenip eklenmeyeceğini alır veya ayarlar. |
| [UsePassim](../../aspose.words.fields/fieldtoa/usepassim/) { get; set; } | Aynı yetkisine ait beş veya daha fazla farklı sayfa referansının, atıfta bulunulan çalışmada bir kelimenin veya pasajın sıklıkla geçtiğini belirtmek için kullanılan "passim" ile değiştirilip değiştirilmeyeceğini alır veya ayarlar. |

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

TA alanları tarafından belirtilen girişlerini kullanarak bir otorite tablosu (yani, bir yasal belgedeki referansların listesi, örneğin, references vakalara, tüzüklere ve kurallara, referansların göründüğü sayfa numaralarıyla birlikte) oluşturur.

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

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)

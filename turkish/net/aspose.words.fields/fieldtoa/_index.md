---
title: FieldToa Class
linktitle: FieldToa
articleTitle: FieldToa
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FieldToa sınıf. TOA alanını uygular C#'da.
type: docs
weight: 2520
url: /tr/net/aspose.words.fields/fieldtoa/
---
## FieldToa class

TOA alanını uygular.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Alanlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fields/) dokümantasyon makalesi.

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
| [BookmarkName](../../aspose.words.fields/fieldtoa/bookmarkname/) { get; set; } | Tabloyu oluşturmak için kullanılan belgenin bölümünü işaretleyen yer işaretinin adını alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [EntryCategory](../../aspose.words.fields/fieldtoa/entrycategory/) { get; set; } | Tabloda yer alan girdilerin integral kategorisini alır veya ayarlar. |
| [EntrySeparator](../../aspose.words.fields/fieldtoa/entryseparator/) { get; set; } | Yetkililer tablosu girişini ve sayfa numarasını ayırmak için kullanılan karakter dizisini alır veya ayarlar. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir alır[`FieldFormat`](../fieldformat/) Alanın formatlamasına yazılı erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucu yeniden hesaplanmamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldtoa/pagenumberlistseparator/) { get; set; } | Sayfa numarası listesindeki iki sayfa numarasını ayırmak için kullanılan karakter sırasını alır veya ayarlar. |
| [PageRangeSeparator](../../aspose.words.fields/fieldtoa/pagerangeseparator/) { get; set; } | Sayfa aralığının başlangıcını ve sonunu ayırmak için kullanılan karakter sırasını alır veya ayarlar. |
| [RemoveEntryFormatting](../../aspose.words.fields/fieldtoa/removeentryformatting/) { get; set; } | Belgedeki giriş metninin formatının yetki tablosundaki girişinden kaldırılıp kaldırılmayacağını alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. Olabilir`hükümsüz` . |
| [SequenceName](../../aspose.words.fields/fieldtoa/sequencename/) { get; set; } | Numarası sayfa numarasına dahil edilen bir dizinin adını alır veya ayarlar. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoa/sequenceseparator/) { get; set; } | Sıra numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter sırasını alır veya ayarlar. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |
| [UseHeading](../../aspose.words.fields/fieldtoa/useheading/) { get; set; } | Yetki tablosundaki girdilere ilişkin kategori başlığının eklenip eklenmeyeceğini alır veya ayarlar. |
| [UsePassim](../../aspose.words.fields/fieldtoa/usepassim/) { get; set; } | Aynı yetkisine yönelik beş veya daha fazla farklı sayfa referansının, alıntı yapılan çalışmada bir kelimenin veya pasajın sıklıkla geçtiğini belirtmek için kullanılan "passim" ile değiştirilip değiştirilmeyeceğini alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son child 'si ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa şunu döndürür:`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alanın bağlantısını kaldırır. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

## Notlar

TA tarafından belirtilen girişlerini kullanarak bir yetki tablosu (yani yasal bir belgedeki davalara, tüzüklere ve kurallara yapılan referanslar gibi referansların bir listesi ve referansların göründüğü sayfa numaralarının bir listesi) oluşturur alanlar.

## Örnekler

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

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)

---
title: FieldToc.HeadingLevelRange
linktitle: HeadingLevelRange
articleTitle: HeadingLevelRange
second_title: .NET için Aspose.Words
description: Gelişmiş içerik organizasyonu ve SEO optimizasyonu için başlık düzeylerini kolayca yönetmek üzere FieldToc HeadingLevelRange özelliğini keşfedin.
type: docs
weight: 80
url: /tr/net/aspose.words.fields/fieldtoc/headinglevelrange/
---
## FieldToc.HeadingLevelRange property

Dahil edilecek başlık düzeyleri aralığını alır veya ayarlar.

```csharp
public string HeadingLevelRange { get; set; }
```

## Örnekler

İçindekiler tablosunun nasıl ekleneceğini ve başlık stillerine göre girdilerle nasıl doldurulacağını gösterir.

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Tüm başlıkları bir içerik tablosuna derleyecek bir TOC alanı ekleyin.
    // Her başlık için bu alan, sola o başlık stilindeki metinle bir satır oluşturacaktır.
    // ve başlığın göründüğü sayfa sağda.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Yalnızca başlıkları listelemek için BookmarkName özelliğini kullanın
    // "MyBookmark" adlı bir yer iminin sınırları içerisinde görünenler.
    field.BookmarkName = "MyBookmark";

    // "Başlık 1" gibi yerleşik bir başlık stili uygulanan metin, başlık olarak sayılır.
    // Bu özellikteki İçindekiler tablosuna göre başlık olarak seçilecek ek stiller ve bunların İçindekiler seviyelerini adlandırabiliriz.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // Varsayılan olarak, Stiller/İçindekiler düzeyleri CustomStyles özelliğinde virgülle ayrılır,
    // ancak bu özellikte özel bir ayırıcı ayarlayabiliriz.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // İçindekiler düzeyi bu aralığın dışında olan başlıkları hariç tutacak şekilde alanı yapılandırın.
    field.HeadingLevelRange = "1-3";

    // İçindekiler tablosu, İçindekiler düzeyi bu aralıkta olan başlıkların sayfa numaralarını görüntülemeyecektir.
    field.PageNumberOmittingLevelRange = "2-5";

     // Her başlığı sayfa numarasından ayıracak özel bir dize ayarlayın.
    field.EntrySeparator = "-";
    field.InsertHyperlinks = true;
    field.HideInWebLayout = false;
    field.PreserveLineBreaks = true;
    field.PreserveTabs = true;
    field.UseParagraphOutlineLevel = false;

    InsertNewPageWithHeading(builder, "First entry", "Heading 1");
    builder.Writeln("Paragraph text.");
    InsertNewPageWithHeading(builder, "Second entry", "Heading 1");
    InsertNewPageWithHeading(builder, "Third entry", "Quote");
    InsertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

    // Bu iki başlığın sayfa numaraları "2-5" aralığında olduğundan atlanacaktır.
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // Bu giriş görünmüyor çünkü "Başlık 4" daha önce belirlediğimiz "1-3" aralığının dışında.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Bu giriş, İçindekiler tablosunda belirtilen yer iminin dışında olduğu için görünmüyor.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

/// <summary>
/// Yeni bir sayfa başlat ve belirtilen stilde bir paragraf ekle.
/// </summary>
public void InsertNewPageWithHeading(DocumentBuilder builder, string captionText, string styleName)
{
    builder.InsertBreak(BreakType.PageBreak);
    string originalStyle = builder.ParagraphFormat.StyleName;
    builder.ParagraphFormat.Style = builder.Document.Styles[styleName];
    builder.Writeln(captionText);
    builder.ParagraphFormat.Style = builder.Document.Styles[originalStyle];
}
```

### Ayrıca bakınız

* class [FieldToc](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

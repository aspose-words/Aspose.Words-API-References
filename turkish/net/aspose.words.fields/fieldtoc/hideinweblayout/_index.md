---
title: FieldToc.HideInWebLayout
second_title: Aspose.Words for .NET API Referansı
description: FieldToc mülk. Web düzeni görünümünde sekme liderinin ve sayfa numaralarının gizlenip gizlenmeyeceğini alır veya ayarlar.
type: docs
weight: 90
url: /tr/net/aspose.words.fields/fieldtoc/hideinweblayout/
---
## FieldToc.HideInWebLayout property

Web düzeni görünümünde sekme liderinin ve sayfa numaralarının gizlenip gizlenmeyeceğini alır veya ayarlar.

```csharp
public bool HideInWebLayout { get; set; }
```

### Örnekler

İçindekiler tablosunun nasıl ekleneceğini ve başlık stillerine göre girdilerle nasıl doldurulacağını gösterir.

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Tüm başlıkları içindekiler tablosunda derleyecek bir TOC alanı ekleyin.
    // Her başlık için bu alan, solda o başlık stilindeki metnin yer aldığı bir satır oluşturacaktır,
    // ve başlığın sağda göründüğü sayfa.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Yalnızca başlıkları listelemek için BookmarkName özelliğini kullanın
    // "MyBookmark" adındaki bir yer iminin sınırları içinde görünenler.
    field.BookmarkName = "MyBookmark";

    // "Başlık 1" gibi yerleşik başlık stilinin uygulandığı metin başlık olarak sayılacaktır.
    // TOC tarafından başlık olarak alınacak ek stilleri ve TOC seviyelerini bu özellikte adlandırabiliriz.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // Varsayılan olarak, Stiller/TOC düzeyleri CustomStyles özelliğinde virgülle ayrılır,
    // ancak bu özellikte özel bir sınırlayıcı ayarlayabiliriz.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // TOC düzeyleri bu aralığın dışında olan başlıkları hariç tutacak şekilde alanı yapılandırın.
    field.HeadingLevelRange = "1-3";

    // TOC, TOC düzeyleri bu aralıkta olan başlıkların sayfa numaralarını görüntülemeyecektir.
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

    // Bu iki başlık "2-5" aralığında olduğundan sayfa numaraları çıkarılacaktır.
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // "Başlık 4" daha önce belirlediğimiz "1-3" aralığının dışında olduğundan bu giriş görünmüyor.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Bu giriş TOC tarafından belirtilen yer iminin dışında olduğundan görünmüyor.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

/// <summary>
/// Yeni bir sayfa başlatın ve belirtilen stilde bir paragraf ekleyin.
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
* ad alanı [Aspose.Words.Fields](../../fieldtoc/)
* toplantı [Aspose.Words](../../../)



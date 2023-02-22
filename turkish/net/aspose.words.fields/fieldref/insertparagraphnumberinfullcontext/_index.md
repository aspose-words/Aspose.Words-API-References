---
title: FieldRef.InsertParagraphNumberInFullContext
second_title: Aspose.Words for .NET API Referansı
description: FieldRef mülk. Başvurulan paragrafın paragraf numarasının tam bağlamda eklenip eklenmeyeceğini alır veya ayarlar.
type: docs
weight: 60
url: /tr/net/aspose.words.fields/fieldref/insertparagraphnumberinfullcontext/
---
## FieldRef.InsertParagraphNumberInFullContext property

Başvurulan paragrafın paragraf numarasının tam bağlamda eklenip eklenmeyeceğini alır veya ayarlar.

```csharp
public bool InsertParagraphNumberInFullContext { get; set; }
```

### Örnekler

Referans yer imlerine REF alanlarının nasıl ekleneceğini gösterir.

```csharp
public void FieldRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #1");
    builder.Write("Text that will appear in REF field");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #2");
    builder.EndBookmark("MyBookmark");
    builder.MoveToDocumentStart();

    // Köşeli parantezlerin şu anda bulunduğumuz liste seviyesini gösterdiği özel bir liste formatı uygulayacağız.
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // Yer imimizdeki metni içerecek, bir köprü görevi görecek ve yer iminin dipnotlarını klonlayacak bir REF alanı ekleyin.
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // Bir REF alanı ekleyin ve başvurulan yer iminin bunun üstünde mi yoksa altında mı olduğunu görüntüleyin.
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // Yer iminin liste numarasını belgede göründüğü şekilde görüntüleyin.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n");
    field.InsertParagraphNumber = true;

    Assert.AreEqual(" REF  MyBookmark \\n", field.GetFieldCode());

    // Yer iminin liste numarasını görüntüleyin, ancak açılı ayraçlar gibi sınırlayıcı olmayan karakterler atlandı.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    // Bir liste düzeyi aşağı git.
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // Yer iminin liste numarasını ve üstündeki tüm liste düzeylerinin numaralarını görüntüleyin.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n");
    field.InsertParagraphNumberInFullContext = true;

    Assert.AreEqual(" REF  MyBookmark \\w", field.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Bu REF alanı ile referans aldığı yer imi arasındaki liste düzeyi numaralarını görüntüleyin.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n");
    field.InsertParagraphNumberInRelativeContext = true;

    Assert.AreEqual(" REF  MyBookmark \\r", field.GetFieldCode());

    // Belgenin sonunda yer imi burada bir liste öğesi olarak görünecektir.
    builder.Writeln("List level above bookmark");
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">>> \x0002";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.REF.docx");

/// <summary>
/// Belge oluşturucunun bir REF alanı eklemesini, onunla bir yer işaretine başvurmasını ve ondan önce ve sonra metin eklemesini sağlayın.
/// </summary>
private static FieldRef InsertFieldRef(DocumentBuilder builder, string bookmarkName, string textBefore, string textAfter)
{
    builder.Write(textBefore);
    FieldRef field = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    field.BookmarkName = bookmarkName;
    builder.Write(textAfter);
    return field;
}
```

### Ayrıca bakınız

* class [FieldRef](../)
* ad alanı [Aspose.Words.Fields](../../fieldref/)
* toplantı [Aspose.Words](../../../)



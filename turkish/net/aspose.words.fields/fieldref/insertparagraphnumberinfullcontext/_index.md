---
title: FieldRef.InsertParagraphNumberInFullContext
linktitle: InsertParagraphNumberInFullContext
articleTitle: InsertParagraphNumberInFullContext
second_title: .NET için Aspose.Words
description: FieldRef InsertParagraphNumberInFullContext özelliğiyle paragraf numaralandırmasını kontrol edin. Gelişmiş belge netliği için referansları kolayca yönetin.
type: docs
weight: 60
url: /tr/net/aspose.words.fields/fieldref/insertparagraphnumberinfullcontext/
---
## FieldRef.InsertParagraphNumberInFullContext property

Başvurulan paragrafın paragraf numarasının tam bağlamda eklenip eklenmeyeceğini alır veya ayarlar.

```csharp
public bool InsertParagraphNumberInFullContext { get; set; }
```

## Örnekler

Yer imlerine referans vermek için REF alanlarının nasıl ekleneceğini gösterir.

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

    // Şu anda hangi liste seviyesinde olduğumuzu gösteren açılı parantez miktarının bulunduğu özel bir liste biçimi uygulayacağız.
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // Yer imimizin içindeki metni içerecek, köprü metni görevi görecek ve yer iminin dipnotlarını kopyalayacak bir REF alanı ekleyin.
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // Bir REF alanı ekle ve başvurulan yer iminin onun üstünde mi yoksa altında mı olduğunu görüntüle.
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // Yer iminin liste numarasını belgede göründüğü gibi görüntüle.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n");
    field.InsertParagraphNumber = true;

    Assert.AreEqual(" REF  MyBookmark \\n", field.GetFieldCode());

    // Yer iminin liste numarasını görüntüler, ancak açılı parantezler gibi sınırlayıcı olmayan karakterleri atlar.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    // Bir liste düzeyi aşağı in.
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // Yer iminin liste numarasını ve üstündeki tüm liste seviyelerinin numaralarını görüntüle.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n");
    field.InsertParagraphNumberInFullContext = true;

    Assert.AreEqual(" REF  MyBookmark \\w", field.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Bu REF alanı ile referans aldığı yer imi arasındaki liste düzeyi numaralarını görüntüle.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n");
    field.InsertParagraphNumberInRelativeContext = true;

    Assert.AreEqual(" REF  MyBookmark \\r", field.GetFieldCode());

    // Belgenin sonunda yer imi burada bir liste öğesi olarak gösterilecektir.
    builder.Writeln("List level above bookmark");
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">>> \x0002";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.REF.docx");
}

/// <summary>
/// Belge oluşturucusunun bir REF alanı eklemesini, bununla bir yer imine referans vermesini ve önüne ve arkasına metin eklemesini sağlayın.
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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

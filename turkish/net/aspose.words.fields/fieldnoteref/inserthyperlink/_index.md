---
title: FieldNoteRef.InsertHyperlink
linktitle: InsertHyperlink
articleTitle: InsertHyperlink
second_title: Aspose.Words for .NET
description: FieldNoteRef InsertHyperlink mülk. Yer imine eklenen paragrafa köprü eklenip eklenmeyeceğini alır veya ayarlar C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldnoteref/inserthyperlink/
---
## FieldNoteRef.InsertHyperlink property

Yer imine eklenen paragrafa köprü eklenip eklenmeyeceğini alır veya ayarlar.

```csharp
public bool InsertHyperlink { get; set; }
```

## Örnekler

NOTEREF alanlarının eklenmesini ve görünümlerinin değiştirilmesini gösterir.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // NOTEREF alanının referans alacağı dipnotlu bir yer imi oluşturun.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // Bu NOTEREF alanı, başvurulan yer iminin içindeki dipnotun numarasını gösterecektir.
    // InsertHyperlink özelliğini ayarlamak, Microsoft Word'deki alanı Ctrl + tıklatarak yer işaretine atlamamızı sağlar.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // \p bayrağı kullanıldığında, dipnot numarasından sonra alan, yer iminin alana göre konumunu da görüntüler.
    // Bookmark1 bu alanın üstündedir ve 1 numaralı dipnot içerir, dolayısıyla güncellemede sonuç "yukarıda 1" olacaktır.
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // Bookmark2 bu alanın altındadır ve 2 numaralı dipnot içerir, dolayısıyla alan "aşağıda 2" olarak görünecektir.
    // \f bayrağı, 2 sayısının asıl metindeki dipnot numarası etiketiyle aynı formatta görünmesini sağlar.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");
}

/// <summary>
/// Belirtilen özelliklere sahip bir NOTEREF alanı eklemek için belge oluşturucuyu kullanır.
/// </summary>
private static FieldNoteRef InsertFieldNoteRef(DocumentBuilder builder, string bookmarkName, bool insertHyperlink, bool insertRelativePosition, bool insertReferenceMark, string textBefore)
{
    builder.Write(textBefore);

    FieldNoteRef field = (FieldNoteRef)builder.InsertField(FieldType.FieldNoteRef, true);
    field.BookmarkName = bookmarkName;
    field.InsertHyperlink = insertHyperlink;
    field.InsertRelativePosition = insertRelativePosition;
    field.InsertReferenceMark = insertReferenceMark;
    builder.Writeln();

    return field;
}

/// <summary>
/// Sonunda dipnot bulunan adlandırılmış bir yer imi eklemek için bir belge oluşturucu kullanır.
/// </summary>
private static void InsertBookmarkWithFootnote(DocumentBuilder builder, string bookmarkName, string bookmarkText, string footnoteText)
{
    builder.StartBookmark(bookmarkName);
    builder.Write(bookmarkText);
    builder.InsertFootnote(FootnoteType.Footnote, footnoteText);
    builder.EndBookmark(bookmarkName);
    builder.Writeln();
}
```

### Ayrıca bakınız

* class [FieldNoteRef](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

---
title: FieldNoteRef.InsertRelativePosition
second_title: Aspose.Words for .NET API Referansı
description: FieldNoteRef mülk. Yer işaretli paragrafın göreli konumunun eklenip eklenmeyeceğini alır veya ayarlar.
type: docs
weight: 50
url: /tr/net/aspose.words.fields/fieldnoteref/insertrelativeposition/
---
## FieldNoteRef.InsertRelativePosition property

Yer işaretli paragrafın göreli konumunun eklenip eklenmeyeceğini alır veya ayarlar.

```csharp
public bool InsertRelativePosition { get; set; }
```

### Örnekler

NOTEREF alanları eklemeyi ve görünümlerini değiştirmeyi gösterir.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // NOTEREF alanının başvuracağı dipnotlu bir yer imi oluşturun.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // Bu NOTEREF alanı, başvurulan yer iminin içindeki dipnot numarasını görüntüler.
    // InsertHyperlink özelliğinin ayarlanması, Microsoft Word'deki alanı Ctrl + tıklatarak yer işaretine atlamamızı sağlar.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // \p bayrağını kullanırken, dipnot numarasından sonra alan, yer iminin alana göre konumunu da görüntüler.
    // Bookmark1 bu alanın üzerindedir ve 1 numaralı dipnot içerir, bu nedenle güncellemede sonuç "yukarıda 1" olacaktır.
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // Bookmark2 bu alanın altındadır ve 2 numaralı dipnot içerir, bu nedenle alan "2 aşağıda" gösterecektir.
    // \f bayrağı, 2 sayısının asıl metindeki dipnot numarası etiketiyle aynı biçimde görünmesini sağlar.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");

/// <summary>
/// Belirtilen özelliklere sahip bir NOTEREF alanı eklemek için bir belge oluşturucu kullanır.
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
* ad alanı [Aspose.Words.Fields](../../fieldnoteref/)
* toplantı [Aspose.Words](../../../)



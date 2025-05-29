---
title: FieldNoteRef.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: .NET için Aspose.Words
description: Gelişmiş organizasyon ve verimlilik için yer imlerinizi kolayca yönetmek ve özelleştirmek amacıyla FieldNoteRef BookmarkName özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldnoteref/bookmarkname/
---
## FieldNoteRef.BookmarkName property

Yer iminin adını alır veya ayarlar.

```csharp
public string BookmarkName { get; set; }
```

## Örnekler

NOTEREF alanlarının nasıl ekleneceğini ve görünümlerinin nasıl değiştirileceğini gösterir.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // NOTEREF alanının referans göstereceği bir dipnot içeren bir yer imi oluşturun.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // Bu NOTEREF alanı, referans verilen yer iminin içindeki dipnotun numarasını görüntüler.
    // InsertHyperlink özelliğini ayarlamak, Microsoft Word'de alana Ctrl + tıklayarak yer imine geçmemizi sağlar.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // \p bayrağı kullanıldığında, dipnot numarasından sonra alan, yer iminin alana göre konumunu da görüntüler.
    // Bookmark1 bu alanın üstündedir ve 1 numaralı dipnotu içermektedir, dolayısıyla güncelleme sırasında sonuç "1 üstte" olacaktır.
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // Bookmark2 bu alanın altındadır ve dipnot numarası 2'yi içerdiğinden, alanda "aşağıda 2" görüntülenecektir.
    // \f bayrağı, 2 sayısının gerçek metindeki dipnot numarası etiketiyle aynı biçimde görünmesini sağlar.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");
}

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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

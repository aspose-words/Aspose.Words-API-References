---
title: FieldPageRef.InsertRelativePosition
linktitle: InsertRelativePosition
articleTitle: InsertRelativePosition
second_title: Aspose.Words for .NET
description: FieldPageRef InsertRelativePosition mülk. Yer imi eklenen paragrafın göreli konumunun eklenip eklenmeyeceğini alır veya ayarlar C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldpageref/insertrelativeposition/
---
## FieldPageRef.InsertRelativePosition property

Yer imi eklenen paragrafın göreli konumunun eklenip eklenmeyeceğini alır veya ayarlar.

```csharp
public bool InsertRelativePosition { get; set; }
```

## Örnekler

Yer imlerinin göreceli konumunu görüntülemek için PAGEREF alanlarının eklenmesini gösterir.

```csharp
public void FieldPageRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);            

    InsertAndNameBookmark(builder, "MyBookmark1");

    // Bir yer iminin hangi sayfada olduğunu gösteren bir PAGEREF alanı ekleyin.
    // Alanın aynı zamanda yer işaretine tıklanabilir bir bağlantı olarak da işlev görmesini sağlamak için InsertHyperlink bayrağını ayarlayın.
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h", 
        InsertFieldPageRef(builder, "MyBookmark3", true, false, "Hyperlink to Bookmark3, on page: ").GetFieldCode());

    // PAGEREF alanının görüntülenmesini sağlamak için \p bayrağını kullanabiliriz
    // yer iminin alanın konumuna göre konumu.
    // Bookmark1 aynı sayfada ve bu alanın üstünde olduğundan, bu alanın görüntülenen sonucu "yukarıda" olacaktır.
    Assert.AreEqual(" PAGEREF  MyBookmark1 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark1", true, true, "Bookmark1 is ").GetFieldCode());

    // Bookmark2 aynı sayfada ve bu alanın altında olacağından bu alanın görüntülenen sonucu "aşağıda" olacaktır.
    Assert.AreEqual(" PAGEREF  MyBookmark2 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark2", true, true, "Bookmark2 is ").GetFieldCode());

    // Bookmark3 farklı bir sayfada olacak, dolayısıyla alan "2. sayfada" olarak görüntülenecektir.
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark3", true, true, "Bookmark3 is ").GetFieldCode());

    InsertAndNameBookmark(builder, "MyBookmark2");
    builder.InsertBreak(BreakType.PageBreak);
    InsertAndNameBookmark(builder, "MyBookmark3");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.PAGEREF.docx");
}

/// <summary>
/// PAGEREF alanı eklemek ve özelliklerini ayarlamak için bir belge oluşturucu kullanır.
/// </summary>
private static FieldPageRef InsertFieldPageRef(DocumentBuilder builder, string bookmarkName, bool insertHyperlink, bool insertRelativePosition, string textBefore)
{
    builder.Write(textBefore);

    FieldPageRef field = (FieldPageRef)builder.InsertField(FieldType.FieldPageRef, true);
    field.BookmarkName = bookmarkName;
    field.InsertHyperlink = insertHyperlink;
    field.InsertRelativePosition = insertRelativePosition;
    builder.Writeln();

    return field;
}

/// <summary>
/// Adlandırılmış bir yer imi eklemek için bir belge oluşturucu kullanır.
/// </summary>
private static void InsertAndNameBookmark(DocumentBuilder builder, string bookmarkName)
{
    builder.StartBookmark(bookmarkName);
    builder.Writeln($"Contents of bookmark \"{bookmarkName}\".");
    builder.EndBookmark(bookmarkName);
}
```

### Ayrıca bakınız

* class [FieldPageRef](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

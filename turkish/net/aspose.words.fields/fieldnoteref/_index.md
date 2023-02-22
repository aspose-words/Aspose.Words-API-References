---
title: Class FieldNoteRef
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.FieldNoteRef sınıf. NOTEREF alanını uygular.
type: docs
weight: 2050
url: /tr/net/aspose.words.fields/fieldnoteref/
---
## FieldNoteRef class

NOTEREF alanını uygular.

```csharp
public class FieldNoteRef : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldNoteRef](fieldnoteref/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldnoteref/bookmarkname/) { get; set; } | Yer iminin adını alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | [`FieldFormat`](../fieldformat/) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [InsertHyperlink](../../aspose.words.fields/fieldnoteref/inserthyperlink/) { get; set; } | Yer işaretli paragrafa bir köprü eklenip eklenmeyeceğini alır veya ayarlar. |
| [InsertReferenceMark](../../aspose.words.fields/fieldnoteref/insertreferencemark/) { get; set; } | Referans işaretini, Dipnot Referansı veya Son Not Referansı stiliyle aynı karakter biçimlendirmesine sahip olarak ekler. |
| [InsertRelativePosition](../../aspose.words.fields/fieldnoteref/insertrelativeposition/) { get; set; } | Yer işaretli paragrafın göreli konumunun eklenip eklenmeyeceğini alır veya ayarlar. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alandan hemen sonra bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğu ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa, döner **hükümsüz** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Bağlantıyı kaldır alanını gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

### Notlar

Belirtilen yer işaretiyle işaretlenen dipnot veya son notun işaretini ekler.

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

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)



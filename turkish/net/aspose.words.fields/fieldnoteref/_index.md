---
title: FieldNoteRef Class
linktitle: FieldNoteRef
articleTitle: FieldNoteRef
second_title: .NET için Aspose.Words
description: NOTEREF alanlarının kusursuz entegrasyonu, belge referanslama ve yönetiminin iyileştirilmesi için Aspose.Words.Fields.FieldNoteRef sınıfını keşfedin.
type: docs
weight: 2610
url: /tr/net/aspose.words.fields/fieldnoteref/
---
## FieldNoteRef class

NOTEREF alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

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
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [InsertHyperlink](../../aspose.words.fields/fieldnoteref/inserthyperlink/) { get; set; } | Yer imlerine eklenen paragrafa bir köprü eklenip eklenmeyeceğini alır veya ayarlar. |
| [InsertReferenceMark](../../aspose.words.fields/fieldnoteref/insertreferencemark/) { get; set; } | Dipnot Referansı veya Sonnot Referansı stiliyle aynı karakter biçimlendirmesiyle referans işaretini ekler. |
| [InsertRelativePosition](../../aspose.words.fields/fieldnoteref/insertrelativeposition/) { get; set; } | Yer imli paragrafın göreli konumunun eklenip eklenmeyeceğini alır veya ayarlar. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son alt 'siyse, üst paragrafını döndürür. Alan zaten kaldırılmışsa, şunu döndürür`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alan bağlantısını kaldırma işlemini gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |

## Notlar

Belirtilen yer imi ile işaretlenen dipnot veya sonnotun işaretini ekler.

## Örnekler

Dipnotların NOTEREF alanıyla nasıl çapraz referanslanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("CrossReference: ");

FieldNoteRef field = (FieldNoteRef)builder.InsertField(FieldType.FieldNoteRef, false); // <--- alanı güncelleme
field.BookmarkName = "CrossRefBookmark";
field.InsertHyperlink = true;
field.InsertReferenceMark = true;
field.InsertRelativePosition = false;
builder.Writeln();

builder.StartBookmark("CrossRefBookmark");
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Cross referenced footnote.");
builder.EndBookmark("CrossRefBookmark");
builder.Writeln();

doc.UpdateFields();

// Bu alan yalnızca Microsoft Word'ün eski sürümlerinde çalışır.
doc.Save(ArtifactsDir + "Field.NOTEREF.doc");
```

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

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)

---
title: FieldSeq.BookmarkName
second_title: Aspose.Words for .NET API Referansı
description: FieldSeq mülk. Geçerli konum yerine belgenin başka bir yerindeki bir öğeye başvuran bir yer imi adı alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldseq/bookmarkname/
---
## FieldSeq.BookmarkName property

Geçerli konum yerine belgenin başka bir yerindeki bir öğeye başvuran bir yer imi adı alır veya ayarlar.

```csharp
public string BookmarkName { get; set; }
```

### Örnekler

İçindekiler ve sıra alanlarının nasıl birleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir TOC alanı, belgede bulunan her SEQ alanı için içindekiler tablosunda bir giriş oluşturabilir.
// Her giriş, SEQ alanını içeren paragrafı içerir,
// ve alanın göründüğü sayfanın numarası.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Bu TOC alanını, "MySequence" değerine sahip bir SequenceIdentifier özelliğine sahip olacak şekilde yapılandırın.
fieldToc.TableOfFiguresLabel = "MySequence";

// Bu TOC alanını yalnızca bir yer iminin sınırları içindeki SEQ alanlarını alacak şekilde yapılandırın
// "TOCBookmark" olarak adlandırıldı.
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// SEQ alanları, her SEQ alanında artan bir sayı görüntüler.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayılar tutar
// SEQ alanının "SequenceIdentifier" özelliği ile tanımlanır.
// İçindekiler ile eşleşen bir dizi tanımlayıcıya sahip bir SEQ alanı ekleyin
// TableOf FiguresLabel özelliği. Bu alan, dışarıda olduğu için TOC'de bir giriş oluşturmaz.
// "Yer İşaretiAdı" tarafından belirlenen yer işaretinin sınırları.
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// Bu SEQ alanının sırası, İçindekiler'in "TableOf FiguresLabel" özelliğiyle eşleşir ve yer iminin sınırları içindedir.
// Bu alanı içeren paragraf, TOC'de bir giriş olarak görünecektir.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// Bu SEQ alanının sırası, İçindekiler'in "TableOf FiguresLabel" özelliğiyle eşleşmiyor,
// ve yer iminin sınırları içinde. Paragrafı TOC'de bir giriş olarak görünmeyecektir.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// Bu SEQ alanının sırası, İçindekiler'in "TableOf FiguresLabel" özelliğiyle eşleşir ve yer iminin sınırları içindedir.
// Bu alan aynı zamanda başka bir yer işaretine de referansta bulunur. Bu yer iminin içeriği, bu SEQ alanı için TOC girişinde görünecektir.
// SEQ alanının kendisi o yer iminin içeriğini göstermeyecektir.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Yukarıdaki SEQ alanı referans aldığı için TOC girişinde görünecek içeriğe sahip bir yer imi oluşturun.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("SEQBookmark");
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", text from inside SEQBookmark.");
builder.EndBookmark("SEQBookmark");

builder.EndBookmark("TOCBookmark");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.Bookmark.docx");
```

### Ayrıca bakınız

* class [FieldSeq](../)
* ad alanı [Aspose.Words.Fields](../../fieldseq/)
* toplantı [Aspose.Words](../../../)



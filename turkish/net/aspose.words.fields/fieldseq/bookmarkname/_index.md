---
title: FieldSeq.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words for .NET
description: FieldSeq BookmarkName mülk. Geçerli konum yerine belgenin başka bir yerindeki bir öğeye başvuran bir yer imi adını alır veya ayarlar C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldseq/bookmarkname/
---
## FieldSeq.BookmarkName property

Geçerli konum yerine belgenin başka bir yerindeki bir öğeye başvuran bir yer imi adını alır veya ayarlar.

```csharp
public string BookmarkName { get; set; }
```

## Örnekler

İçindekiler tablosu ile sıra alanlarının nasıl birleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir TOC alanı, belgede bulunan her bir SEQ alanı için içindekiler tablosunda bir giriş oluşturabilir.
// Her giriş SEQ alanını içeren paragrafı içerir,
// ve alanın göründüğü sayfanın numarası.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Bu TOC alanını "MySequence" değerine sahip bir SequenceIdentifier özelliğine sahip olacak şekilde yapılandırın.
fieldToc.TableOfFiguresLabel = "MySequence";

// Bu TOC alanını yalnızca bir yer iminin sınırları içindeki SEQ alanlarını alacak şekilde yapılandırın
// "TOCBookmark" olarak adlandırıldı.
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// SEQ alanları, her SEQ alanında artan bir sayım görüntüler.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayıları korur
// SEQ alanının "SequenceIdentifier" özelliği tarafından tanımlanır.
// TOC'lerle eşleşen bir sıra tanımlayıcıya sahip bir SEQ alanı ekleyin
// TableOfFigürlerLabel özelliği. Bu alan, TOC'nin dışında olduğundan, TOC'de bir giriş oluşturmayacaktır.
// "Yer İşaretiAdı" tarafından belirlenen yer iminin sınırları.
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// Bu SEQ alanının sırası TOC'nin "TableOfFigürlerLabel" özelliğiyle eşleşir ve yer iminin sınırları dahilindedir.
// Bu alanı içeren paragraf, TOC'de bir giriş olarak görünecektir.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// Bu SEQ alanının sırası TOC'nin "TableOfFigürleriLabel" özelliğiyle eşleşmiyor,
// ve yer iminin sınırları dahilindedir. Paragrafı TOC'de bir giriş olarak görünmeyecektir.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// Bu SEQ alanının sırası, TOC'nin "TableOfFigürlerLabel" özelliğiyle eşleşir ve yer işaretinin sınırları dahilindedir.
// Bu alan aynı zamanda başka bir yer imine de başvuruyor. Bu yer iminin içeriği bu SEQ alanının İçindekiler girişinde görünecektir.
// SEQ alanının kendisi bu yer iminin içeriğini görüntülemeyecektir.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Yukarıdaki SEQ alanının ona referans vermesi nedeniyle TOC girişinde görünecek içeriğe sahip bir yer imi oluşturun.
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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

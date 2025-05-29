---
title: FieldSeq.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: .NET için Aspose.Words
description: Belge gezintisini kolayca yönetmek için FieldSeq BookmarkName özelliğini keşfedin. Sorunsuz öğe referansı için yer imi adlarını ayarlayın veya alın.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldseq/bookmarkname/
---
## FieldSeq.BookmarkName property

Geçerli konumdan ziyade belgenin başka bir yerindeki bir öğeye atıfta bulunan bir yer imi adını alır veya ayarlar.

```csharp
public string BookmarkName { get; set; }
```

## Örnekler

İçindekiler tablosu ve sıra alanlarının nasıl birleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir TOC alanı, belgede bulunan her SEQ alanı için içerik tablosunda bir giriş oluşturabilir.
// Her giriş, SEQ alanını içeren paragrafı içerir.
// ve alanın göründüğü sayfanın numarası.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Bu TOC alanını "MySequence" değerine sahip bir SequenceIdentifier özelliğine sahip olacak şekilde yapılandırın.
fieldToc.TableOfFiguresLabel = "MySequence";

// Bu TOC alanını yalnızca bir yer imi sınırları içindeki SEQ alanlarını alacak şekilde yapılandırın
// "TOCBookmark" olarak adlandırıldı.
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// SEQ alanları her SEQ alanında artan bir sayım görüntüler.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayımları korur
// SEQ alanının "SequenceIdentifier" özelliği ile tanımlanır.
// İçindekiler tablosuyla eşleşen bir dizi tanımlayıcısına sahip bir SEQ alanı ekleyin
// TableOfFiguresLabel özelliği. Bu alan, TOC'de bir giriş oluşturmaz çünkü dışarıdadır
// "BookmarkName" ile belirtilen yer iminin sınırları.
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// Bu SEQ alanının dizisi, TOC'nin "TableOfFiguresLabel" özelliğiyle eşleşiyor ve yer iminin sınırları içinde.
// Bu alanı içeren paragraf, İçindekiler tablosunda bir giriş olarak gösterilecektir.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// Bu SEQ alanının dizisi TOC'nin "TableOfFiguresLabel" özelliğiyle eşleşmiyor,
// ve yer iminin sınırları içindedir. Paragrafı TOC'de bir giriş olarak görünmeyecektir.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// Bu SEQ alanının dizisi, TOC'nin "TableOfFiguresLabel" özelliğiyle eşleşiyor ve yer iminin sınırları içinde.
// Bu alan başka bir yer imine de başvurur. Bu yer iminin içerikleri bu SEQ alanının TOC girişinde görünecektir.
// SEQ alanı, söz konusu yer iminin içeriğini görüntülemeyecektir.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Yukarıdaki SEQ alanının referans vermesi nedeniyle TOC girişinde gösterilecek içeriklere sahip bir yer imi oluşturun.
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

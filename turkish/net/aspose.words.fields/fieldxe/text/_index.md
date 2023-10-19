---
title: FieldXE.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: FieldXE Text mülk. Girişin metnini alır veya ayarlar C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words.fields/fieldxe/text/
---
## FieldXE.Text property

Girişin metnini alır veya ayarlar.

```csharp
public string Text { get; set; }
```

## Örnekler

Bir INDEX alanının nasıl oluşturulacağını ve ardından onu girişlerle doldurmak için XE alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir giriş görüntüleyecek bir INDEX alanı oluşturun.
// Her girişte XE alanının Text özelliği değeri sol tarafta görüntülenecektir
// ve sağda XE alanını içeren sayfa.
// XE alanlarının "Text" özelliğinde aynı değer varsa,
// INDEX alanı bunları tek bir girişte gruplandıracaktır.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// INDEX alanını yalnızca sınırlar içindeki XE alanlarını görüntüleyecek şekilde yapılandırın
// "MainBookmark" adlı ve "EntryType" özellikleri "A" değerine sahip olan bir yer işaretinin.
// Hem INDEX hem de XE alanları için "EntryType" özelliği dize değerinin yalnızca ilk karakterini kullanır.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// Yeni bir sayfada yer imini değerle eşleşen bir adla başlatın
// INDEX alanının "BookmarkName" özelliğinin.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// INDEX alanı bu girişi alacaktır çünkü bu yer iminin içindedir,
// ve giriş türü aynı zamanda INDEX alanının giriş türüyle de eşleşir.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Giriş türleri eşleşmediğinden INDEX'te görünmeyecek bir XE alanı ekleyin.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Yer imini sonlandırın ve ardından bir XE alanı ekleyin.
// INDEX alanıyla aynı türdedir ancak görünmez
// yer iminin sınırlarının dışında olduğundan.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

Bir INDEX alanının XE alanlarını kullanarak girişlerle nasıl doldurulacağını ve ayrıca görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir giriş görüntüleyecek bir INDEX alanı oluşturun.
// Her girişte XE alanının Text özelliği değeri sol tarafta görüntülenecektir,
// ve sağdaki XE alanını içeren sayfanın numarası.
// XE alanlarının "Text" özelliğinde aynı değer varsa,
// INDEX alanı bunları tek bir girişte gruplandıracaktır.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Bu özelliğin değerini "A" olarak ayarlamak tüm girişleri ilk harflerine göre gruplandıracaktır,
// ve o harfi her grubun üstüne büyük harfle yerleştir.
index.Heading = "A";

// INDEX alanı tarafından oluşturulan tabloyu 2 sütuna yayılacak şekilde ayarlayın.
index.NumberOfColumns = "2";

// "ac" karakter aralığının dışında kalan başlangıç harflerine sahip tüm girişleri atlanacak şekilde ayarlayın.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Sonraki iki XE alanı "A" başlığı altında görünecek,
// ilgili metin stilleri sayfa numaralarına da uygulanır.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";
indexEntry.IsItalic = true;

Assert.AreEqual(" XE  Apple \\i", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apricot";
indexEntry.IsBold = true;

Assert.AreEqual(" XE  Apricot \\b", indexEntry.GetFieldCode());

// Sonraki iki XE alanının her ikisi de INDEX alanları içindekiler tablosunda "B" ve "C" başlığı altında olacaktır.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// INDEX alanları tüm girişleri alfabetik olarak sıralar, böylece bu giriş diğer ikisiyle birlikte "A" altında görünecektir.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Bu girdi "D" harfiyle başladığı için görünmeyecektir,
// INDEX alanının LetterRange özelliğinin tanımladığı "ac" karakter aralığının dışındadır.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Ayrıca bakınız

* class [FieldXE](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

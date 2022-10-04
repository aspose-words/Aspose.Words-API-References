---
title: Text
second_title: Aspose.Words for .NET API Referansı
description: Girdi metnini alır veya ayarlar.
type: docs
weight: 70
url: /tr/net/aspose.words.fields/fieldxe/text/
---
## FieldXE.Text property

Girdi metnini alır veya ayarlar.

```csharp
public string Text { get; set; }
```

### Örnekler

Bir INDEX alanının nasıl oluşturulacağını ve ardından onu girdilerle doldurmak için XE alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir giriş görüntüleyecek bir INDEX alanı oluşturun.
// Her giriş, XE alanının Metin özellik değerini sol tarafta gösterecek
// ve sağda XE alanını içeren sayfa.
// XE alanları "Text" özelliğinde aynı değere sahipse,
// INDEX alanı bunları tek bir girişte gruplayacaktır.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// INDEX alanını yalnızca sınırlar içindeki XE alanlarını gösterecek şekilde yapılandırın
// "MainBookmark" adlı ve "EntryType" özellikleri "A" değerine sahip bir yer işaretinin.
// Hem INDEX hem de XE alanları için "EntryType" özelliği, dize değerinin yalnızca ilk karakterini kullanır.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// Yeni bir sayfada, yer imini değerle eşleşen bir adla başlatın
// INDEX alanının "Yer İşaretiAdı" özelliğinin.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// INDEX alanı, yer iminin içinde olduğu için bu girişi alacaktır,
// ve onun giriş tipi de INDEX alanının giriş tipiyle eşleşir.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Giriş türleri eşleşmediği için INDEX'te görünmeyecek bir XE alanı ekleyin.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Yer imini sonlandırın ve ardından bir XE alanı ekleyin.
// INDEX alanıyla aynı türdendir, ancak görünmeyecektir
// yer iminin sınırlarının dışında olduğu için.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

Bir INDEX alanının XE alanlarını kullanarak girişlerle nasıl doldurulacağını ve görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir giriş görüntüleyecek bir INDEX alanı oluşturun.
// Her giriş, sol tarafta XE alanının Text özellik değerini gösterecek,
// ve sağdaki XE alanını içeren sayfanın numarası.
// XE alanları "Text" özelliğinde aynı değere sahipse,
// INDEX alanı bunları tek bir girişte gruplayacaktır.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Bu özelliğin değerini "A" olarak ayarlamak, tüm girişleri ilk harflerine göre gruplayacaktır,
// ve o harfi her grubun üstüne büyük harfle yerleştirin.
index.Heading = "A";

// INDEX alanı tarafından oluşturulan tabloyu 2 sütuna yayılacak şekilde ayarlayın.
index.NumberOfColumns = "2";

// "ac" karakter aralığının dışında başlangıç harfleri olan tüm girişleri atlanacak şekilde ayarlayın.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Sonraki iki XE alanı "A" başlığının altında görünecek,
// sayfa numaralarına da uygulanmış ilgili metin stilleriyle.
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

// INDEX alanları tüm girdileri alfabetik olarak sıralar, bu nedenle bu girdi diğer ikisi ile birlikte "A" altında görünecektir.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Bu girdi "D" harfiyle başladığı için görünmeyecek,
// INDEX alanının LetterRange özelliğinin tanımladığı "ac" karakter aralığının dışında olan.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Ayrıca bakınız

* class [FieldXE](../)
* ad alanı [Aspose.Words.Fields](../../fieldxe/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

---
title: FieldXE.Text
linktitle: Text
articleTitle: Text
second_title: .NET için Aspose.Words
description: FieldXE metin özelliğinizi zahmetsizce yönetin. Sorunsuz veri işleme ve gelişmiş kullanıcı deneyimi için giriş metnini kolayca alın veya ayarlayın.
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

INDEX alanının nasıl oluşturulacağını ve ardından XE alanlarının bu alanı girişlerle nasıl dolduracağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir girdi görüntüleyecek bir INDEX alanı oluşturun.
// Her giriş, sol tarafta XE alanının Metin özelliği değerini gösterecektir
// ve sağ tarafta XE alanını içeren sayfa.
// XE alanlarının "Metin" özelliğinde aynı değer varsa,
// INDEX alanı bunları tek bir girdide gruplayacaktır.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// INDEX alanını yalnızca sınırlar içindeki XE alanlarını görüntüleyecek şekilde yapılandırın
// "MainBookmark" adlı ve "EntryType" özelliklerinin değeri "A" olan bir yer iminin.
// Hem INDEX hem de XE alanları için, "EntryType" özelliği dize değerinin yalnızca ilk karakterini kullanır.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// Yeni bir sayfada, yer imini değerle eşleşen bir adla başlatın
// INDEX alanının "BookmarkName" özelliği.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// INDEX alanı bu girişi alacaktır çünkü yer iminin içindedir,
// ve giriş tipi de INDEX alanının giriş tipiyle eşleşiyor.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Giriş türleri eşleşmediği için DİZİN'de görünmeyecek bir XE alanı ekleyin.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Yer imini sonlandır ve ardından bir XE alanı ekle.
// INDEX alanıyla aynı türdedir, ancak görünmeyecektir
// yer imi sınırlarının dışında olduğundan.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

XE alanlarını kullanarak bir INDEX alanının nasıl girdilerle doldurulacağını ve görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir girdi görüntüleyecek bir INDEX alanı oluşturun.
// Her giriş, sol tarafta XE alanının Metin özelliği değerini görüntüler,
// ve sağ tarafta XE alanını içeren sayfanın numarası.
// XE alanlarının "Metin" özelliğinde aynı değer varsa,
// INDEX alanı bunları tek bir girdide gruplayacaktır.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Bu özelliğin değerini "A" olarak ayarlamak tüm girdileri ilk harflerine göre gruplandıracaktır,
// ve her grubun üstüne o harfi büyük harfle yaz.
index.Heading = "A";

// INDEX alanıyla oluşturulan tabloyu 2 sütuna yayılacak şekilde ayarla.
index.NumberOfColumns = "2";

// "ac" karakter aralığının dışında başlayan harflere sahip tüm girdilerin atlanmasını ayarla.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Sonraki iki XE alanı "A" başlığı altında gösterilecektir.
// kendi metin stilleri sayfa numaralarına da uygulandı.
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

// Sonraki iki XE alanı, INDEX alanları içindekiler tablosunda "B" ve "C" başlığı altında yer alacaktır.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// INDEX alanları tüm girdileri alfabetik olarak sıralar, bu nedenle bu girdi diğer ikisiyle birlikte "A" altında gösterilir.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Bu giriş "D" harfiyle başladığı için görünmeyecektir.
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

---
title: FieldIndex.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words for .NET
description: FieldIndex BookmarkName mülk. Dizini oluşturmak için kullanılan belgenin bölümünü işaretleyen yer işaretinin adını alır veya ayarlar C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldindex/bookmarkname/
---
## FieldIndex.BookmarkName property

Dizini oluşturmak için kullanılan belgenin bölümünü işaretleyen yer işaretinin adını alır veya ayarlar.

```csharp
public string BookmarkName { get; set; }
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

### Ayrıca bakınız

* class [FieldIndex](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

---
title: FieldIndex.EntryType
linktitle: EntryType
articleTitle: EntryType
second_title: .NET için Aspose.Words
description: Optimize edilmiş dizinleme ve gelişmiş arama performansı için dizin girişi türlerini verimli bir şekilde yönetmek üzere FieldIndex EntryType özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldindex/entrytype/
---
## FieldIndex.EntryType property

Dizini oluşturmak için kullanılan bir dizin giriş türünü alır veya ayarlar.

```csharp
public string EntryType { get; set; }
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

### Ayrıca bakınız

* class [FieldIndex](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

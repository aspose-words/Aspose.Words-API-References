---
title: FieldXE.Yomi
second_title: Aspose.Words for .NET API Referansı
description: FieldXE mülk. Dizin girişi için yomiyi dizinleri sıralamak için ilk fonetik karakter alır veya ayarlar
type: docs
weight: 80
url: /tr/net/aspose.words.fields/fieldxe/yomi/
---
## FieldXE.Yomi property

Dizin girişi için yomi'yi (dizinleri sıralamak için ilk fonetik karakter) alır veya ayarlar

```csharp
public string Yomi { get; set; }
```

### Örnekler

INDEX alanı girişlerinin fonetik olarak nasıl sıralanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir giriş görüntüleyecek bir INDEX alanı oluşturun.
// Her giriş, sol tarafta XE alanının Text özellik değerini gösterecek,
// ve sağdaki XE alanını içeren sayfanın numarası.
// INDEX girişi, "Metin" özelliğinde eşleşen değerlere sahip tüm XE alanlarını toplayacaktır.
// her XE alanı için bir giriş yapmak yerine tek bir girişe.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// INDEX tablosu, girdilerini Metin özelliklerinin değerlerine göre alfabetik sırayla otomatik olarak sıralar.
// Girişleri fonetik olarak Hiragana kullanarak sıralamak için INDEX tablosunu ayarlayın.
index.UseYomi = sortEntriesUsingYomi;

if (sortEntriesUsingYomi)
    Assert.AreEqual(" INDEX  \\y", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX ", index.GetFieldCode());

// INDEX alanının içindekiler tablosunda giriş olarak görünecek 4 XE alanı ekleyin.
// "Metin" özelliği, telaffuzu belirsiz olabilen Kanji'de bir kelimenin yazılışını içerebilir,
// kelimenin "Yomi" versiyonu tam olarak Hiragana kullanılarak nasıl telaffuz edildiğini heceleyecek.
// INDEX alanımızı Yomi kullanacak şekilde ayarlarsak bu girdileri sıralayacaktır.
// Metin değerleri yerine Yomi özelliklerinin değerine göre.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "愛子";
indexEntry.Yomi = "あ";

Assert.AreEqual(" XE  愛子 \\y あ", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "明美";
indexEntry.Yomi = "あ";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "恵美";
indexEntry.Yomi = "え";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "愛美";
indexEntry.Yomi = "え";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Yomi.docx");
```

### Ayrıca bakınız

* class [FieldXE](../)
* ad alanı [Aspose.Words.Fields](../../fieldxe/)
* toplantı [Aspose.Words](../../../)



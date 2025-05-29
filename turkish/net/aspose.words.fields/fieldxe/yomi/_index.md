---
title: FieldXE.Yomi
linktitle: Yomi
articleTitle: Yomi
second_title: .NET için Aspose.Words
description: FieldXE Yomi özelliğiyle dizin girişlerinizi optimize edin, gelişmiş veri organizasyonu için ilk fonetik karakteri kullanarak verimli sıralama yapın.
type: docs
weight: 80
url: /tr/net/aspose.words.fields/fieldxe/yomi/
---
## FieldXE.Yomi property

Dizin girişi için yomi'yi (dizinleri sıralamak için ilk fonetik karakter) alır veya ayarlar

```csharp
public string Yomi { get; set; }
```

## Örnekler

INDEX alan girişlerinin fonetik olarak nasıl sıralanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir girdi görüntüleyecek bir INDEX alanı oluşturun.
// Her giriş, sol tarafta XE alanının Metin özelliği değerini görüntüler,
// ve sağ tarafta XE alanını içeren sayfanın numarası.
// INDEX girişi, "Metin" özelliğindeki eşleşen değerlere sahip tüm XE alanlarını toplayacaktır
// her XE alanı için bir giriş yapmak yerine, tek bir girişe.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// INDEX tablosu, girdilerini otomatik olarak Metin özelliklerinin değerlerine göre alfabetik sıraya göre sıralar.
// INDEX tablosunu Hiragana kullanarak girdileri fonetik olarak sıralayacak şekilde ayarlayın.
index.UseYomi = sortEntriesUsingYomi;

if (sortEntriesUsingYomi)
    Assert.AreEqual(" INDEX  \\y", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX ", index.GetFieldCode());

// INDEX alanının içerik tablosunda giriş olarak gösterilecek 4 XE alanı ekleyin.
// "Metin" özelliği, telaffuzu belirsiz olabilen bir kelimenin Kanji dilindeki yazımını içerebilir.
// "Yomi" versiyonu ise kelimenin Hiragana kullanılarak telaffuz edildiği gibi yazılacak.
// INDEX alanımızı Yomi kullanacak şekilde ayarlarsak, bu girdileri sıralayacaktır
// Metin değerleri yerine Yomi özelliklerinin değeriyle.
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

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Yomi.docx");
```

### Ayrıca bakınız

* class [FieldXE](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

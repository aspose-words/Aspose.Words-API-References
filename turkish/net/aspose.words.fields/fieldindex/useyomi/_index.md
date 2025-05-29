---
title: FieldIndex.UseYomi
linktitle: UseYomi
articleTitle: UseYomi
second_title: .NET için Aspose.Words
description: FieldIndex UseYomi özelliğiyle dizinlemenizi geliştirin. Gelişmiş arama görünürlüğü ve daha iyi kullanıcı deneyimi için yomi metnini kolayca etkinleştirin.
type: docs
weight: 170
url: /tr/net/aspose.words.fields/fieldindex/useyomi/
---
## FieldIndex.UseYomi property

Dizin girişleri için yomi metninin kullanımının etkinleştirilip etkinleştirilmeyeceğini alır veya ayarlar.

```csharp
public bool UseYomi { get; set; }
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

* class [FieldIndex](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

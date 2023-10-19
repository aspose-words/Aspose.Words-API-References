---
title: FieldXE.Yomi
linktitle: Yomi
articleTitle: Yomi
second_title: Aspose.Words for .NET
description: FieldXE Yomi mülk. Dizin girişi için yomiyi indeksleri sıralamak için ilk fonetik karakter alır veya ayarlar C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words.fields/fieldxe/yomi/
---
## FieldXE.Yomi property

Dizin girişi için yomi'yi (indeksleri sıralamak için ilk fonetik karakter) alır veya ayarlar

```csharp
public string Yomi { get; set; }
```

## Örnekler

INDEX alanı girişlerinin fonetik olarak nasıl sıralanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir giriş görüntüleyecek bir INDEX alanı oluşturun.
// Her girişte XE alanının Text özelliği değeri sol tarafta görüntülenecektir,
// ve sağdaki XE alanını içeren sayfanın numarası.
// INDEX girişi "Text" özelliğinde eşleşen değerlere sahip tüm XE alanlarını toplayacaktır
// her XE alanı için bir giriş yapmak yerine tek bir girişe.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// INDEX tablosu, girişlerini Metin özelliklerinin değerlerine göre alfabetik sıraya göre otomatik olarak sıralar.
// INDEX tablosunu, bunun yerine Hiragana'yı kullanarak girişleri fonetik olarak sıralayacak şekilde ayarlayın.
index.UseYomi = sortEntriesUsingYomi;

if (sortEntriesUsingYomi)
    Assert.AreEqual(" INDEX  \\y", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX ", index.GetFieldCode());

// INDEX alanının içindekiler tablosunda giriş olarak görünecek 4 XE alanı ekleyin.
// "Text" özelliği, telaffuzu belirsiz olabilecek bir kelimenin Kanji dilinde yazılışını içerebilir,
// kelimenin "Yomi" versiyonu Hiragana kullanıldığında tam olarak nasıl telaffuz edildiğini yazacaktır.
// INDEX alanımızı Yomi kullanacak şekilde ayarlarsak bu girdileri sıralayacaktır
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

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Yomi.docx");
```

### Ayrıca bakınız

* class [FieldXE](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

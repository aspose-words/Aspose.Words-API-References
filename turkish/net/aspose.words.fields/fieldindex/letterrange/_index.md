---
title: FieldIndex.LetterRange
linktitle: LetterRange
articleTitle: LetterRange
second_title: .NET için Aspose.Words
description: Belirli bir harf aralığını verimli bir şekilde ayarlamak veya almak için FieldIndex LetterRange özelliğini keşfedin ve dizinleme performansınızı optimize edin.
type: docs
weight: 90
url: /tr/net/aspose.words.fields/fieldindex/letterrange/
---
## FieldIndex.LetterRange property

Dizin sınırını belirleyen harf aralığını alır veya ayarlar.

```csharp
public string LetterRange { get; set; }
```

## Örnekler

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

* class [FieldIndex](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

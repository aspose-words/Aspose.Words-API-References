---
title: FieldIndex.RunSubentriesOnSameLine
second_title: Aspose.Words for .NET API Referansı
description: FieldIndex mülk. Alt girişlerin ana girişle aynı satırda çalıştırılıp çalıştırılmayacağını alır veya ayarlar.
type: docs
weight: 140
url: /tr/net/aspose.words.fields/fieldindex/runsubentriesonsameline/
---
## FieldIndex.RunSubentriesOnSameLine property

Alt girişlerin ana girişle aynı satırda çalıştırılıp çalıştırılmayacağını alır veya ayarlar.

```csharp
public bool RunSubentriesOnSameLine { get; set; }
```

### Örnekler

INDEX alanındaki alt girişlerle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir giriş görüntüleyecek bir INDEX alanı oluşturun.
// Her girişte XE alanının Text özelliği değeri sol tarafta görüntülenecektir,
// ve sağdaki XE alanını içeren sayfanın numarası.
// INDEX girişi "Text" özelliğinde eşleşen değerlere sahip tüm XE alanlarını toplayacaktır
// her XE alanı için bir giriş yapmak yerine tek bir girişe.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.PageNumberSeparator = ", see page ";
index.Heading = "A";

// Değeri INDEX girişinin başlığı olan Text özelliğine sahip XE alanları.
// Bu değer iki nokta üst üste işaretiyle bölünmüş iki dize parçası içeriyorsa (INDEX girişi :) sınırlayıcıyı işleyecektir,
// ilk bölüm başlıktır ve ikinci bölüm alt başlık olacaktır.
// INDEX alanı önce girişleri alfabetik olarak gruplandırır, ardından aynı değere sahip birden fazla XE alanı varsa
// başlıklar, INDEX alanı bunları bu başlıkların değerlerine göre ayrıca alt gruplara ayıracaktır.
// Kaç kez olduğuna bağlı olarak birden fazla alt gruplandırma katmanı olabilir
// XE alanlarının Metin özellikleri bu şekilde bölümlere ayrılır.
// Varsayılan olarak bir INDEX alanı giriş grubu, bu grup içindeki her alt başlık için yeni bir satır oluşturacaktır.
// Başlığı korumak için RunSubentriesOnSameLine bayrağını true olarak ayarlayabiliriz,
// ve bunun yerine grup için tüm alt başlıklar tek satırda yer alacak, bu da INDEX alanını daha kompakt hale getirecek.
index.RunSubentriesOnSameLine = runSubentriesOnTheSameLine;

if (runSubentriesOnTheSameLine)
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A \\r", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A", index.GetFieldCode());

// Her biri yeni bir sayfaya ve "Başlık 1" adlı aynı başlığa sahip iki XE alanı ekleyin,
// INDEX alanının bunları gruplamak için kullanacağı.
// RunSubentriesOnSameLine false ise INDEX tablosu üç satır oluşturacaktır:
// "Başlık 1" gruplandırma başlığı için bir satır ve her alt başlık için bir satır daha.
// RunSubentriesOnSameLine doğruysa INDEX tablosu tek satırlık bir tablo oluşturacaktır
// başlığı ve her alt başlığı kapsayan giriş.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 1";

Assert.AreEqual(" XE  \"Heading 1:Subheading 1\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 2";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + $"Field.INDEX.XE.Subheading.docx");
```

### Ayrıca bakınız

* class [FieldIndex](../)
* ad alanı [Aspose.Words.Fields](../../fieldindex/)
* toplantı [Aspose.Words](../../../)



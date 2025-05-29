---
title: FieldIndex.RunSubentriesOnSameLine
linktitle: RunSubentriesOnSameLine
articleTitle: RunSubentriesOnSameLine
second_title: .NET için Aspose.Words
description: Ana girdilerle birlikte alt girdileri kolayca yönetmek ve böylece veri organizasyonunu kolaylaştırmak için FieldIndex RunSubentriesOnSameLine özelliğini keşfedin.
type: docs
weight: 140
url: /tr/net/aspose.words.fields/fieldindex/runsubentriesonsameline/
---
## FieldIndex.RunSubentriesOnSameLine property

Alt girdilerin ana girdiyle aynı satıra çalıştırılıp çalıştırılmayacağını alır veya ayarlar.

```csharp
public bool RunSubentriesOnSameLine { get; set; }
```

## Örnekler

INDEX alanındaki alt girdilerle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir girdi görüntüleyecek bir INDEX alanı oluşturun.
// Her giriş, sol tarafta XE alanının Metin özelliği değerini görüntüler,
// ve sağ tarafta XE alanını içeren sayfanın numarası.
// INDEX girişi, "Metin" özelliğindeki eşleşen değerlere sahip tüm XE alanlarını toplayacaktır
// her XE alanı için bir giriş yapmak yerine, tek bir girişe.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.PageNumberSeparator = ", see page ";
index.Heading = "A";

// Değeri INDEX girişinin başlığı olan bir Metin özelliğine sahip XE alanları.
// Bu değer iki nokta üst üste ile bölünmüş iki dize parçası içeriyorsa (INDEX girişi :) ayırıcısını ele alacaktır),
// ilk bölüm başlık olacak ve ikinci bölüm alt başlık olacak.
// INDEX alanı önce girdileri alfabetik olarak gruplandırır, ardından aynı dizine sahip birden fazla XE alanı varsa
// başlıklar, INDEX alanı bunları bu başlıkların değerlerine göre daha da alt gruplandıracaktır.
// Kaç kez alt gruplama yapılacağına bağlı olarak birden fazla alt gruplama katmanı olabilir.
// XE alanlarının Metin özellikleri bu şekilde segmentlere ayrılır.
// Varsayılan olarak, bir INDEX alan girişi grubu, bu gruptaki her alt başlık için yeni bir satır oluşturacaktır.
// Başlığı korumak için RunSubentriesOnSameLine bayrağını true olarak ayarlayabiliriz.
// ve grubun her alt başlığını tek satırda yazın, bu da INDEX alanını daha kompakt hale getirecektir.
index.RunSubentriesOnSameLine = runSubentriesOnTheSameLine;

if (runSubentriesOnTheSameLine)
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A \\r", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A", index.GetFieldCode());

// Her biri yeni bir sayfada ve aynı başlıkla "Başlık 1" adlı iki XE alanı ekleyin,
// INDEX alanının bunları gruplamak için kullanacağı.
// Eğer RunSubentriesOnSameLine false ise, INDEX tablosu üç satır oluşturacaktır:
// "Başlık 1" gruplama başlığı için bir satır ve her alt başlık için bir satır daha.
// RunSubentriesOnSameLine true ise, INDEX tablosu tek satırlık bir
// Başlığı ve her alt başlığı kapsayan girdi.
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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

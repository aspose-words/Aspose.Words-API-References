---
title: FieldIndex.HasSequenceName
linktitle: HasSequenceName
articleTitle: HasSequenceName
second_title: .NET için Aspose.Words
description: FieldIndex HasSequenceName özelliğiyle verimli alan sonucu oluşturma için bir diziye ihtiyaç olup olmadığını keşfedin. Veri yönetiminizi bugün optimize edin!
type: docs
weight: 60
url: /tr/net/aspose.words.fields/fieldindex/hassequencename/
---
## FieldIndex.HasSequenceName property

Alanın sonucu oluşturulurken bir dizinin kullanılıp kullanılmayacağını belirten bir değer alır.

```csharp
public bool HasSequenceName { get; }
```

## Örnekler

INDEX ve SEQ alanlarını birleştirerek bir belgenin nasıl parçalara bölüneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir girdi görüntüleyecek bir INDEX alanı oluşturun.
// Her giriş, sol tarafta XE alanının Metin özelliği değerini görüntüler,
// ve sağ tarafta XE alanını içeren sayfanın numarası.
// XE alanlarının "Metin" özelliğinde aynı değer varsa,
// INDEX alanı bunları tek bir girdide gruplayacaktır.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// SequenceName özelliğinde, bir SEQ alanı dizisi adı verin. Bu INDEX alanının her girişi artık şu şekilde de görüntülenecektir:
// Bu girişi oluşturan XE alan konumundaki sıra sayısının bulunduğu sayı.
index.SequenceName = "MySequence";

// Kullanıcıya anlamlarını açıklayacak şekilde dizi ve sayfa numaralarının etrafına metin yerleştirin.
// Bu yapılandırmayla oluşturulan bir giriş, sayfa numarasında "MySequence at 1 on page 1" benzeri bir şey gösterecektir.
// PageNumberSeparator ve SequenceSeparator 15 karakterden uzun olamaz.
index.PageNumberSeparator = "\tMySequence at ";
index.SequenceSeparator = " on page ";
Assert.IsTrue(index.HasSequenceName);

Assert.AreEqual(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.GetFieldCode());

// SEQ alanları her SEQ alanında artan bir sayım görüntüler.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayımları korur
// SEQ alanının "SequenceIdentifier" özelliği ile tanımlanır.
// "MySequence" dizisini 1'e taşıyan bir SEQ alanı ekleyin.
// Bu alan normal belge metninden farklı değildir. Bir INDEX alanının içerik tablosunda görünmez.
builder.InsertBreak(BreakType.PageBreak);
FieldSeq sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", sequenceField.GetFieldCode());

// INDEX alanına bir giriş oluşturacak bir XE alanı ekleyin.
// "MySequence" 1'de olduğundan ve bu XE alanı 2. sayfada olduğundan, yukarıda tanımladığımız özel ayırıcılarla birlikte,
// bu alanın INDEX girişi sol tarafta "Cat", sağ tarafta ise "MySequence at 1 on page 2" ifadesini gösterecektir.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

Assert.AreEqual(" XE  Cat", indexEntry.GetFieldCode());

// Bir sayfa sonu ekleyin ve "MySequence"ı 3'e ilerletmek için SEQ alanlarını kullanın.
builder.InsertBreak(BreakType.PageBreak);
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

// Yukarıdakiyle aynı Metin özelliğine sahip bir XE alanı ekleyin.
// INDEX girişi, "Metin" özelliğindeki eşleşen değerlere sahip XE alanlarını gruplayacaktır
// her XE alanı için bir giriş yapmak yerine, tek bir girişe.
// 2. sayfada olduğumuzdan ve "MySequence" 3. sayfada olduğundan, ", 3 on page 3" yukarıdakiyle aynı INDEX girişine eklenecektir.
// Bu DİZİN girişinin sayfa numarası kısmı artık "MySequence 1'de 2. sayfada, 3'te 3. sayfada" ifadesini görüntüleyecektir.
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

// Yeni ve benzersiz bir Metin özelliği değerine sahip bir XE alanı ekleyin.
// Bu, 4. sayfada MySequence'in 3. sırada olduğu yeni bir giriş ekleyecektir.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Dog";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Sequence.docx");
```

### Ayrıca bakınız

* class [FieldIndex](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

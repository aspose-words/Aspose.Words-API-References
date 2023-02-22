---
title: FieldIndex.SequenceName
second_title: Aspose.Words for .NET API Referansı
description: FieldIndex mülk. Numarası sayfa numarasına dahil olan bir dizinin adını alır veya ayarlar.
type: docs
weight: 150
url: /tr/net/aspose.words.fields/fieldindex/sequencename/
---
## FieldIndex.SequenceName property

Numarası sayfa numarasına dahil olan bir dizinin adını alır veya ayarlar.

```csharp
public string SequenceName { get; set; }
```

### Örnekler

INDEX ve SEQ alanlarını birleştirerek bir belgenin nasıl bölümlere ayrılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir giriş görüntüleyecek bir INDEX alanı oluşturun.
// Her giriş, sol tarafta XE alanının Text özellik değerini gösterecek,
// ve sağdaki XE alanını içeren sayfanın numarası.
// XE alanları "Text" özelliğinde aynı değere sahipse,
// INDEX alanı bunları tek bir girişte gruplayacaktır.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// SequenceName özelliğinde, bir SEQ alanı dizisi adlandırın. Bu INDEX alanının her girişi artık aynı zamanda görüntülenecektir.
// bu girişi oluşturan XE alanı konumunda dizi sayımının açık olduğu sayı.
index.SequenceName = "MySequence";

// Kullanıcıya anlamlarını açıklamak için sıra ve sayfa numaralarının etrafında olacak metni ayarlayın.
// Bu konfigürasyonla oluşturulan bir giriş, sayfa numarasında "Sayfa 1'de MySequence at 1" gibi bir şey görüntüleyecektir.
// PageNumberSeparator ve SequenceSeparator 15 karakterden uzun olamaz.
index.PageNumberSeparator = "\tMySequence at ";
index.SequenceSeparator = " on page ";
Assert.IsTrue(index.HasSequenceName);

Assert.AreEqual(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.GetFieldCode());

// SEQ alanları, her SEQ alanında artan bir sayı görüntüler.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayılar tutar
// SEQ alanının "SequenceIdentifier" özelliği ile tanımlanır.
// "MySequence" dizisini 1'e taşıyan bir SEQ alanı ekleyin.
// Bu alan normal belge metninden farklı değildir. Bir INDEX alanının içindekiler tablosunda görünmeyecektir.
builder.InsertBreak(BreakType.PageBreak);
FieldSeq sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", sequenceField.GetFieldCode());

// INDEX alanına bir giriş oluşturacak bir XE alanı ekleyin.
// "MySequence" 1'de olduğundan ve bu XE alanı yukarıda tanımladığımız özel ayırıcılarla birlikte 2. sayfada olduğundan,
// bu alanın INDEX girişi, sol tarafta "Cat" ve sağ tarafta "MySequence at 1 on page 2" görüntüleyecektir.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

Assert.AreEqual(" XE  Cat", indexEntry.GetFieldCode());

// Bir sayfa sonu ekleyin ve "MySequence" ı 3'e ilerletmek için SEQ alanlarını kullanın.
builder.InsertBreak(BreakType.PageBreak);
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

// Yukarıdaki ile aynı Text özelliğine sahip bir XE alanı ekleyin.
// INDEX girişi, "Metin" özelliğinde eşleşen değerlere sahip XE alanlarını gruplayacaktır
// her XE alanı için bir giriş yapmak yerine tek bir girişe.
// 3. sayfada "MySequence" ile 2. sayfada olduğumuz için, ", 3 sayfa 3" yukarıdakiyle aynı INDEX girişine eklenecektir.
// Bu INDEX girişinin sayfa numarası kısmı şimdi "Sayfa 2'de 1'de MySequence, sayfa 3'te 3" görüntüleyecektir.
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

// Yeni ve benzersiz bir Metin özelliği değerine sahip bir XE alanı ekleyin.
// Bu, MySequence sayfa 4'te 3'te olacak şekilde yeni bir giriş ekleyecektir.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Dog";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Sequence.docx");
```

### Ayrıca bakınız

* class [FieldIndex](../)
* ad alanı [Aspose.Words.Fields](../../fieldindex/)
* toplantı [Aspose.Words](../../../)



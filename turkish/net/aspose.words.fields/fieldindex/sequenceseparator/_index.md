---
title: FieldIndex.SequenceSeparator
linktitle: SequenceSeparator
articleTitle: SequenceSeparator
second_title: Aspose.Words for .NET
description: FieldIndex SequenceSeparator mülk. Sıra numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter sırasını alır veya ayarlar C#'da.
type: docs
weight: 160
url: /tr/net/aspose.words.fields/fieldindex/sequenceseparator/
---
## FieldIndex.SequenceSeparator property

Sıra numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter sırasını alır veya ayarlar.

```csharp
public string SequenceSeparator { get; set; }
```

## Örnekler

INDEX ve SEQ alanlarını birleştirerek bir belgenin nasıl bölümlere bölüneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir giriş görüntüleyecek bir INDEX alanı oluşturun.
// Her girişte XE alanının Text özelliği değeri sol tarafta görüntülenecektir,
// ve sağdaki XE alanını içeren sayfanın numarası.
// XE alanlarının "Text" özelliğinde aynı değer varsa,
// INDEX alanı bunları tek bir girişte gruplandıracaktır.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// SıraAdı özelliğinde, bir SEQ alanı dizisine ad verin. Bu INDEX alanının her girişi artık aynı zamanda görüntülenecektir
// bu girişi oluşturan XE alanı konumunda sıra sayısının açık olduğu sayı.
index.SequenceName = "MySequence";

// Kullanıcıya anlamlarını açıklayacak şekilde sıra ve sayfa numaralarının etrafında olacak metni ayarlayın.
// Bu konfigürasyonla oluşturulan bir girdinin sayfa numarasında "MySequence at 1 on page 1" gibi bir şey görüntülenecektir.
// PageNumberSeparator ve SequenceSeparator 15 karakterden uzun olamaz.
index.PageNumberSeparator = "\tMySequence at ";
index.SequenceSeparator = " on page ";
Assert.IsTrue(index.HasSequenceName);

Assert.AreEqual(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.GetFieldCode());

// SEQ alanları, her SEQ alanında artan bir sayım görüntüler.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayıları korur
// SEQ alanının "SequenceIdentifier" özelliği tarafından tanımlanır.
// "MySequence" dizisini 1'e taşıyan bir SEQ alanı ekleyin.
// Bu alanın normal belge metninden hiçbir farkı yoktur. Bir INDEX alanının içindekiler tablosunda görünmez.
builder.InsertBreak(BreakType.PageBreak);
FieldSeq sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", sequenceField.GetFieldCode());

// INDEX alanına giriş oluşturacak bir XE alanı ekleyin.
// "MySequence" 1'de olduğundan ve bu XE alanı yukarıda tanımladığımız özel ayırıcılarla birlikte 2. sayfada olduğundan,
// bu alanın INDEX girişi sol tarafta "Cat" ve sağ tarafta "MySequence 1, sayfa 2" görüntüleyecektir.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

Assert.AreEqual(" XE  Cat", indexEntry.GetFieldCode());

// Bir sayfa sonu ekleyin ve "MySequence"ı 3'e ilerletmek için SEQ alanlarını kullanın.
builder.InsertBreak(BreakType.PageBreak);
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

// Yukarıdakiyle aynı Text özelliğine sahip bir XE alanı ekleyin.
// INDEX girişi, XE alanlarını "Metin" özelliğinde eşleşen değerlerle gruplandırır
// her XE alanı için bir giriş yapmak yerine tek bir girişe.
// "MySequence" 3'teyken 2. sayfada olduğumuzdan, ", 3 sayfa 3'te" yukarıdaki gibi aynı INDEX girişine eklenecektir.
// Bu INDEX girişinin sayfa numarası kısmında artık "MySequence 1 sayfa 2, 3 sayfa 3" görüntülenecektir.
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

// Yeni ve benzersiz bir Metin özelliği değerine sahip bir XE alanı ekleyin.
// Bu, sayfa 4'te MySequence 3'te olacak şekilde yeni bir giriş ekleyecektir.
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

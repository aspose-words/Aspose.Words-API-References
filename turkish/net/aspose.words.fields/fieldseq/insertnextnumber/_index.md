---
title: FieldSeq.InsertNextNumber
second_title: Aspose.Words for .NET API Referansı
description: FieldSeq mülk. Belirtilen öğe için sonraki sıra numarasının eklenip eklenmeyeceğini alır veya ayarlar.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldseq/insertnextnumber/
---
## FieldSeq.InsertNextNumber property

Belirtilen öğe için sonraki sıra numarasının eklenip eklenmeyeceğini alır veya ayarlar.

```csharp
public bool InsertNextNumber { get; set; }
```

### Örnekler

SEQ alanlarını kullanarak numaralandırma oluşturmayı gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// SEQ alanları, her SEQ alanında artan bir sayı görüntüler.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayılar tutar
// SEQ alanının "SequenceIdentifier" özelliği ile tanımlanır.
// "MySequence"ın geçerli sayım değerini gösterecek bir SEQ alanı ekleyin,
// 100'e ayarlamak için "ResetNumber" özelliğini kullandıktan sonra.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// Bu dizideki bir sonraki sayıyı başka bir SEQ alanı ile göster.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// 1. düzey bir başlık girin.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Aynı diziden başka bir SEQ alanı ekleyin ve her başlıktaki sayımı 1 ile sıfırlayacak şekilde yapılandırın.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// Yukarıdaki başlık 1. seviye başlıktır, bu nedenle bu dizinin sayısı 1'e sıfırlanır.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// Bu dizinin bir sonraki numarasına git.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.InsertNextNumber = true;
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\n", fieldSeq.GetFieldCode());
Assert.AreEqual("2", fieldSeq.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.ResetNumbering.docx");
```

### Ayrıca bakınız

* class [FieldSeq](../)
* ad alanı [Aspose.Words.Fields](../../fieldseq/)
* toplantı [Aspose.Words](../../../)



---
title: FieldSeq.ResetHeadingLevel
linktitle: ResetHeadingLevel
articleTitle: ResetHeadingLevel
second_title: .NET için Aspose.Words
description: FieldSeq ResetHeadingLevel özelliğini keşfedin, sıra numaralarını sıfırlayarak başlık seviyelerini kolayca yönetin. Belge biçimlendirmenizi bugün basitleştirin!
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldseq/resetheadinglevel/
---
## FieldSeq.ResetHeadingLevel property

Sıra numarasını sıfırlamak için başlık seviyesini temsil eden bir tam sayı alır veya ayarlar. Sayı yoksa -1 döndürür.

```csharp
public string ResetHeadingLevel { get; set; }
```

## Örnekler

SEQ alanlarını kullanarak numaralandırma oluşturmayı gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// SEQ alanları her SEQ alanında artan bir sayım görüntüler.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayımları korur
// SEQ alanının "SequenceIdentifier" özelliği ile tanımlanır.
// "MySequence"ın geçerli sayım değerini görüntüleyecek bir SEQ alanı ekleyin,
// "ResetNumber" özelliğini kullanarak 100'e ayarladıktan sonra.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// Bu dizideki bir sonraki sayıyı başka bir SEQ alanıyla görüntüle.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// 1. seviye bir başlık ekle.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Aynı diziden başka bir SEQ alanı ekle ve her başlıkta 1 ile sayımı sıfırlayacak şekilde yapılandır.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// Yukarıdaki başlık 1. seviye bir başlık olduğundan, bu dizinin sayısı 1 olarak sıfırlanır.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// Bu dizinin bir sonraki sayısına geç.
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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

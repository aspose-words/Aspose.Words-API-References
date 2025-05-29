---
title: FieldAutoNum.SeparatorCharacter
linktitle: SeparatorCharacter
articleTitle: SeparatorCharacter
second_title: .NET için Aspose.Words
description: FieldAutoNum SeparatorCharacter özelliğini keşfedin, gelişmiş veri biçimlendirme ve iyileştirilmiş kullanılabilirlik için ayırıcı karakterinizi kolayca özelleştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldautonum/separatorcharacter/
---
## FieldAutoNum.SeparatorCharacter property

Kullanılacak ayırıcı karakteri alır veya ayarlar.

```csharp
public string SeparatorCharacter { get; set; }
```

## Örnekler

Paragrafların otomatik sayı alanlarını kullanarak nasıl numaralandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Her AUTONUM alanı, çalışan AUTONUM alanlarının geçerli sayısını görüntüler,
// Numaralandırılmış bir liste gibi öğeleri otomatik olarak numaralandırmamıza olanak tanır.
// Bu alanda "1." sayısı gösterilecektir.
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// Alan sonucunda sayıdan hemen sonra görünen ayırıcı karakter varsayılan olarak noktadır.
// Bu özelliği null bırakırsak, ikinci AUTONUM alanımız belgede "2." gösterecektir.
Assert.IsNull(field.SeparatorCharacter);

// Bu özelliği, dizesinin ilk karakterini yeni ayırıcı karakter olarak uygulayacak şekilde ayarlayabiliriz.
// Bu durumda AUTONUM alanımız artık "2:" değerini gösterecektir.
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### Ayrıca bakınız

* class [FieldAutoNum](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

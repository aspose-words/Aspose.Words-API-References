---
title: FieldAutoNum.SeparatorCharacter
linktitle: SeparatorCharacter
articleTitle: SeparatorCharacter
second_title: Aspose.Words for .NET
description: FieldAutoNum SeparatorCharacter mülk. Kullanılacak ayırıcı karakteri alır veya ayarlar C#'da.
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

Autonum alanlarını kullanarak paragrafların nasıl numaralandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Her AUTONUM alanı, devam eden AUTONUM alanı sayısının geçerli değerini görüntüler,
// numaralı liste gibi öğeleri otomatik olarak numaralandırmamıza izin veriyor.
// Bu alanda "1" sayısı görüntülenecektir.
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// Alan sonucunda sayıdan hemen sonra görünen ayırıcı karakter, varsayılan olarak noktadır.
// Bu özelliği null bırakırsak ikinci AUTONUM alanımız "2" olarak görünecektir. belgede.
Assert.IsNull(field.SeparatorCharacter);

// Bu özelliği, dizesinin ilk karakterini yeni ayırıcı karakter olarak uygulayacak şekilde ayarlayabiliriz.
// Bu durumda AUTONUM alanımız artık "2:" görüntüleyecektir.
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### Ayrıca bakınız

* class [FieldAutoNum](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

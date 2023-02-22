---
title: FieldAutoNum.SeparatorCharacter
second_title: Aspose.Words for .NET API Referansı
description: FieldAutoNum mülk. Kullanılacak ayırıcı karakteri alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldautonum/separatorcharacter/
---
## FieldAutoNum.SeparatorCharacter property

Kullanılacak ayırıcı karakteri alır veya ayarlar.

```csharp
public string SeparatorCharacter { get; set; }
```

### Örnekler

Otomatik sayı alanlarını kullanarak paragrafların nasıl numaralandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Her AUTONUM alanı, çalışan bir AUTONUM alan sayısının mevcut değerini görüntüler,
// numaralı bir liste gibi öğeleri otomatik olarak numaralandırmamıza izin veriyor.
// Bu alan "1" sayısını gösterecektir.
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// Sayının hemen ardından alan sonucunda görünen ayırıcı karakter, varsayılan olarak bir noktadır.
// Bu özelliği boş bırakırsak, ikinci AUTONUM alanımız "2"yi gösterecektir. belgede.
Assert.IsNull(field.SeparatorCharacter);

// Bu özelliği, dizesinin ilk karakterini yeni ayırıcı karakter olarak uygulayacak şekilde ayarlayabiliriz.
// Bu durumda AUTONUM alanımız artık "2:" görüntüleyecektir.
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### Ayrıca bakınız

* class [FieldAutoNum](../)
* ad alanı [Aspose.Words.Fields](../../fieldautonum/)
* toplantı [Aspose.Words](../../../)



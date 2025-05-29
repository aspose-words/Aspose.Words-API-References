---
title: FieldChar.FieldType
linktitle: FieldType
articleTitle: FieldType
second_title: .NET için Aspose.Words
description: Alanın türünü ortaya çıkaran, veri yönetiminizi ve programlama verimliliğinizi artıran FieldChar FieldType özelliğini keşfedin. Şimdi daha fazlasını öğrenin!
type: docs
weight: 10
url: /tr/net/aspose.words.fields/fieldchar/fieldtype/
---
## FieldChar.FieldType property

Alanın türünü döndürür.

```csharp
public FieldType FieldType { get; }
```

## Örnekler

FieldStart düğümüyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.Format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

FieldChar fieldStart = field.Start;

Assert.AreEqual(FieldType.FieldDate, fieldStart.FieldType);
Assert.AreEqual(false, fieldStart.IsDirty);
Assert.AreEqual(false, fieldStart.IsLocked);

// Belgedeki alanı temsil eden cephe nesnesini al.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Alanı güncel tarihi gösterecek şekilde güncelleyin.
field.Update();
```

### Ayrıca bakınız

* enum [FieldType](../../fieldtype/)
* class [FieldChar](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

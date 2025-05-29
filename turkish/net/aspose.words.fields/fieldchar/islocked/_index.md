---
title: FieldChar.IsLocked
linktitle: IsLocked
articleTitle: IsLocked
second_title: .NET için Aspose.Words
description: FieldChar IsLocked özelliğini keşfedin, alan yeniden hesaplamasını kolaylıkla kontrol edin. Belgenizin doğruluğunu ve verimliliğini bugün artırın!
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldchar/islocked/
---
## FieldChar.IsLocked property

Üst alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır).

```csharp
public bool IsLocked { get; set; }
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

* class [FieldChar](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

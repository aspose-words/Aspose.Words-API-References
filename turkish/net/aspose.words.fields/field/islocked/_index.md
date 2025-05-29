---
title: Field.IsLocked
linktitle: IsLocked
articleTitle: IsLocked
second_title: .NET için Aspose.Words
description: Alanlar için IsLocked özelliğini keşfedin—yeniden hesaplamayı kontrol edin ve veri bütünlüğünü geliştirin. Veri sonuçlarınızın verimli yönetimini bugün açın!
type: docs
weight: 50
url: /tr/net/aspose.words.fields/field/islocked/
---
## Field.IsLocked property

Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır).

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

* class [Field](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

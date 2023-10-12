---
title: Field.IsLocked
second_title: Aspose.Words for .NET API Referansı
description: Field mülk. Alanın kilitli olup olmadığını alır veya ayarlar sonucu yeniden hesaplanmamalıdır.
type: docs
weight: 50
url: /tr/net/aspose.words.fields/field/islocked/
---
## Field.IsLocked property

Alanın kilitli olup olmadığını alır veya ayarlar (sonucu yeniden hesaplanmamalıdır).

```csharp
public bool IsLocked { get; set; }
```

### Örnekler

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

// Belgedeki alanı temsil eden cephe nesnesini alın.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Geçerli tarihi gösterecek şekilde alanı güncelleyin.
field.Update();
```

### Ayrıca bakınız

* class [Field](../)
* ad alanı [Aspose.Words.Fields](../../field/)
* toplantı [Aspose.Words](../../../)



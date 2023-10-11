---
title: FieldChar.IsLocked
second_title: Aspose.Words for .NET API Referansı
description: FieldChar mülk. Ana alanın kilitli olup olmadığını alır veya ayarlar sonucu yeniden hesaplanmamalıdır.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldchar/islocked/
---
## FieldChar.IsLocked property

Ana alanın kilitli olup olmadığını alır veya ayarlar (sonucu yeniden hesaplanmamalıdır).

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

* class [FieldChar](../)
* ad alanı [Aspose.Words.Fields](../../fieldchar/)
* toplantı [Aspose.Words](../../../)



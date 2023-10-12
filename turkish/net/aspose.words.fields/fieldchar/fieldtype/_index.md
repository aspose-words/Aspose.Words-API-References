---
title: FieldChar.FieldType
second_title: Aspose.Words for .NET API Referansı
description: FieldChar mülk. Alanın türünü döndürür.
type: docs
weight: 10
url: /tr/net/aspose.words.fields/fieldchar/fieldtype/
---
## FieldChar.FieldType property

Alanın türünü döndürür.

```csharp
public FieldType FieldType { get; }
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

* enum [FieldType](../../fieldtype/)
* class [FieldChar](../)
* ad alanı [Aspose.Words.Fields](../../fieldchar/)
* toplantı [Aspose.Words](../../../)



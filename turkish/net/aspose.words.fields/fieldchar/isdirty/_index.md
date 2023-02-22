---
title: FieldChar.IsDirty
second_title: Aspose.Words for .NET API Referansı
description: FieldChar mülk. Alandaki geçerli sonucun belgede yapılan diğer değişiklikler nedeniyle artık doğru eski olup olmadığını alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldchar/isdirty/
---
## FieldChar.IsDirty property

Alandaki geçerli sonucun belgede yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar.

```csharp
public bool IsDirty { get; set; }
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

// Geçerli tarihi göstermek için alanı güncelleyin.
field.Update();
```

### Ayrıca bakınız

* class [FieldChar](../)
* ad alanı [Aspose.Words.Fields](../../fieldchar/)
* toplantı [Aspose.Words](../../../)



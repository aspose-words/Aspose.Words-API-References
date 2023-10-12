---
title: FieldChar.GetField
second_title: Aspose.Words for .NET API Referansı
description: FieldChar yöntem. char. alanı için bir alan döndürür
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldchar/getfield/
---
## FieldChar.GetField method

char. alanı için bir alan döndürür

```csharp
public Field GetField()
```

### Geri dönüş değeri

Alan karakteri için bir alan.

### Notlar

Yeni bir[`Field`](../../field/) Yöntem her çağrıldığında nesne oluşturulur.

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

* class [Field](../../field/)
* class [FieldChar](../)
* ad alanı [Aspose.Words.Fields](../../fieldchar/)
* toplantı [Aspose.Words](../../../)



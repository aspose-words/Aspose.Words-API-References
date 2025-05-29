---
title: FieldChar.GetField
linktitle: GetField
articleTitle: GetField
second_title: .NET için Aspose.Words
description: FieldChar'daki GetField metodunu keşfedin, uygulamalarınızda optimum veri yönetimi ve gelişmiş performans için alanları zahmetsizce alın.
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

char alanı için bir alan.

## Notlar

Yeni bir[`Field`](../../field/) nesne, yöntem her çağrıldığında oluşturulur.

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

* class [Field](../../field/)
* class [FieldChar](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)

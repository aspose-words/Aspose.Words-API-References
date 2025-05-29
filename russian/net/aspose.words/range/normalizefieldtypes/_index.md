---
title: Range.NormalizeFieldTypes
linktitle: NormalizeFieldTypes
articleTitle: NormalizeFieldTypes
second_title: Aspose.Words для .NET
description: Преобразуйте типы полей с помощью метода NormalizeFieldTypes. Убедитесь, что FieldStart, FieldSeparator и FieldEnd соответствуют указанным кодам полей для бесперебойной обработки данных.
type: docs
weight: 90
url: /ru/net/aspose.words/range/normalizefieldtypes/
---
## Range.NormalizeFieldTypes method

Изменяет значения типа поля[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) из[`FieldStart`](../../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../../aspose.words.fields/fieldend/) в этом диапазоне, чтобы они соответствовали типам полей, содержащимся в кодах полей.

```csharp
public void NormalizeFieldTypes()
```

## Примечания

Используйте этот метод после внесения изменений в документ, влияющих на типы полей.

Чтобы изменить значения типа поля во всем документе, используйте[`NormalizeFieldTypes`](../../document/normalizefieldtypes/).

## Примеры

Показывает, как поддерживать тип поля в актуальном состоянии с помощью его кода поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// Aspose.Words автоматически определяет типы полей на основе кодов полей.
Assert.AreEqual(FieldType.FieldDate, field.Type);

// Вручную измените необработанный текст поля, который определяет код поля.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];
fieldText.Text = "PAGE";

// Изменение кода поля изменило тип этого поля на другой,
// но свойства типа поля по-прежнему отображают старый тип.
Assert.AreEqual("PAGE", field.GetFieldCode());
Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual(FieldType.FieldDate, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.End.FieldType);

// Обновите эти свойства с помощью этого метода, чтобы отобразить текущее значение.
doc.NormalizeFieldTypes();

Assert.AreEqual(FieldType.FieldPage, field.Type);
Assert.AreEqual(FieldType.FieldPage, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldPage, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldPage, field.End.FieldType);
```

### Смотрите также

* class [Range](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

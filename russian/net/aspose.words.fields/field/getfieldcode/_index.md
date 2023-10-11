---
title: Field.GetFieldCode
second_title: Справочник по API Aspose.Words для .NET
description: Field метод. Возвращает текст между началом поля и разделителем поля или концом поля если разделителя нет. Включены как код поля так и результат поля дочерних полей.
type: docs
weight: 110
url: /ru/net/aspose.words.fields/field/getfieldcode/
---
## GetFieldCode() {#getfieldcode}

Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат поля дочерних полей.

```csharp
public string GetFieldCode()
```

### Примеры

Показывает, как вставить поле в документ с помощью кода поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Эта перегрузка метода InsertField автоматически обновляет вставленные поля.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

Показывает, как получить код поля поля.

```csharp
// Открытие документа, содержащего поле MERGEFIELD внутри поля IF.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Есть два способа получить код поля поля:
// 1 - Опустить внутренние поля:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - Включить его внутренние поля:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// По умолчанию метод GetFieldCode отображает внутренние поля.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Смотрите также

* class [Field](../)
* пространство имен [Aspose.Words.Fields](../../field/)
* сборка [Aspose.Words](../../../)

---

## GetFieldCode(bool) {#getfieldcode_1}

Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет).

```csharp
public string GetFieldCode(bool includeChildFieldCodes)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| includeChildFieldCodes | Boolean | `истинный` если должны быть включены коды дочерних полей. |

### Примеры

Показывает, как получить код поля поля.

```csharp
// Открытие документа, содержащего поле MERGEFIELD внутри поля IF.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Есть два способа получить код поля поля:
// 1 - Опустить внутренние поля:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - Включить его внутренние поля:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// По умолчанию метод GetFieldCode отображает внутренние поля.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Смотрите также

* class [Field](../)
* пространство имен [Aspose.Words.Fields](../../field/)
* сборка [Aspose.Words](../../../)



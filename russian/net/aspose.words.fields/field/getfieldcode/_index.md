---
title: Field.GetFieldCode
linktitle: GetFieldCode
articleTitle: GetFieldCode
second_title: Aspose.Words для .NET
description: Откройте для себя метод GetFieldCode, легко извлекайте текст между началом поля и разделителем, включая коды дочерних полей и результаты. Повысьте эффективность кодирования!
type: docs
weight: 110
url: /ru/net/aspose.words.fields/field/getfieldcode/
---
## GetFieldCode() {#getfieldcode}

Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). Включаются как код поля, так и результат поля дочерних полей.

```csharp
public string GetFieldCode()
```

## Примеры

Показывает, как вставить поле в документ, используя код поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Эта перегрузка метода InsertField автоматически обновляет вставленные поля.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

Показывает, как получить код поля.

```csharp
// Открываем документ, содержащий MERGEFIELD внутри поля IF.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Получить код поля можно двумя способами:
// 1 - Пропустить внутренние поля:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - Включить его внутренние поля:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// По умолчанию метод GetFieldCode отображает внутренние поля.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Смотрите также

* class [Field](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)

---

## GetFieldCode(*bool*) {#getfieldcode_1}

Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует).

```csharp
public string GetFieldCode(bool includeChildFieldCodes)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| includeChildFieldCodes | Boolean | `истинный` если необходимо включить коды дочерних полей. |

## Примеры

Показывает, как получить код поля.

```csharp
// Открываем документ, содержащий MERGEFIELD внутри поля IF.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Получить код поля можно двумя способами:
// 1 - Пропустить внутренние поля:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - Включить его внутренние поля:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// По умолчанию метод GetFieldCode отображает внутренние поля.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Смотрите также

* class [Field](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)

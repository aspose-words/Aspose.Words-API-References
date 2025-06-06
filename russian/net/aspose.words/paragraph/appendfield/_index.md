---
title: Paragraph.AppendField
linktitle: AppendField
articleTitle: AppendField
second_title: Aspose.Words для .NET
description: Улучшите свой документ с помощью метода Paragraph AppendField, легко добавляя пользовательские поля в абзацы для лучшей организации и ясности.
type: docs
weight: 260
url: /ru/net/aspose.words/paragraph/appendfield/
---
## AppendField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#appendfield}

Добавляет поле к этому абзацу.

```csharp
public Field AppendField(FieldType fieldType, bool updateField)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldType | FieldType | Тип поля для добавления. |
| updateField | Boolean | Указывает, следует ли немедленно обновить поле. |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field/) объект, представляющий добавленное поле.

## Примеры

Показаны различные способы добавления полей в абзац.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Ниже приведены три способа добавления поля в конец абзаца.
// 1 — Добавить поле ДАТА, используя тип поля, а затем обновить его:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - Добавить поле ВРЕМЯ, используя код поля:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Добавьте поле QUOTE, используя код поля, и заставьте его отображать значение-заполнитель:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Это поле будет отображать свое значение-заполнитель, пока мы его не обновим.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Смотрите также

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## AppendField(*string*) {#appendfield_1}

Добавляет поле к этому абзацу.

```csharp
public Field AppendField(string fieldCode)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | String | Код поля для добавления (без фигурных скобок). |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field/) объект, представляющий добавленное поле.

## Примеры

Показаны различные способы добавления полей в абзац.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Ниже приведены три способа добавления поля в конец абзаца.
// 1 — Добавить поле ДАТА, используя тип поля, а затем обновить его:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - Добавить поле ВРЕМЯ, используя код поля:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Добавьте поле QUOTE, используя код поля, и заставьте его отображать значение-заполнитель:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Это поле будет отображать свое значение-заполнитель, пока мы его не обновим.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Смотрите также

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## AppendField(*string, string*) {#appendfield_2}

Добавляет поле к этому абзацу.

```csharp
public Field AppendField(string fieldCode, string fieldValue)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | String | Код поля для добавления (без фигурных скобок). |
| fieldValue | String | Значение поля для добавления. Пройти`нулевой` для полей, не имеющих значения. |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field/) объект, представляющий добавленное поле.

## Примеры

Показаны различные способы добавления полей в абзац.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Ниже приведены три способа добавления поля в конец абзаца.
// 1 — Добавить поле ДАТА, используя тип поля, а затем обновить его:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - Добавить поле ВРЕМЯ, используя код поля:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Добавьте поле QUOTE, используя код поля, и заставьте его отображать значение-заполнитель:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Это поле будет отображать свое значение-заполнитель, пока мы его не обновим.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Смотрите также

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---
title: Paragraph.AppendField
second_title: Справочник по API Aspose.Words для .NET
description: Paragraph метод. Добавляет поле к этому абзацу.
type: docs
weight: 260
url: /ru/net/aspose.words/paragraph/appendfield/
---
## AppendField(FieldType, bool) {#appendfield}

Добавляет поле к этому абзацу.

```csharp
public Field AppendField(FieldType fieldType, bool updateField)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldType | FieldType | Тип добавляемого поля. |
| updateField | Boolean | Указывает, следует ли немедленно обновить поле. |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field/) объект, представляющий добавленное поле.

### Примеры

Показывает различные способы добавления полей в абзац.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Ниже приведены три способа добавления поля в конец абзаца.
// 1 — добавить поле ДАТА, используя тип поля, а затем обновить его:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 — добавить поле ВРЕМЯ, используя код поля:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 — Добавьте поле ЦИТАТЫ, используя код поля, и заставьте его отображать значение заполнителя:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// В этом поле будет отображаться значение заполнителя, пока мы его не обновим.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Смотрите также

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Paragraph](../)
* пространство имен [Aspose.Words](../../paragraph/)
* сборка [Aspose.Words](../../../)

---

## AppendField(string) {#appendfield_1}

Добавляет поле к этому абзацу.

```csharp
public Field AppendField(string fieldCode)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | String | Код поля для добавления (без фигурных скобок). |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field/) объект, представляющий добавленное поле.

### Примеры

Показывает различные способы добавления полей в абзац.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Ниже приведены три способа добавления поля в конец абзаца.
// 1 — добавить поле ДАТА, используя тип поля, а затем обновить его:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 — добавить поле ВРЕМЯ, используя код поля:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 — Добавьте поле ЦИТАТЫ, используя код поля, и заставьте его отображать значение заполнителя:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// В этом поле будет отображаться значение заполнителя, пока мы его не обновим.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Смотрите также

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* пространство имен [Aspose.Words](../../paragraph/)
* сборка [Aspose.Words](../../../)

---

## AppendField(string, string) {#appendfield_2}

Добавляет поле к этому абзацу.

```csharp
public Field AppendField(string fieldCode, string fieldValue)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | String | Код поля для добавления (без фигурных скобок). |
| fieldValue | String | Значение поля для добавления. Проходить`нулевой` для полей, которые не имеют значения. |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field/) объект, представляющий добавленное поле.

### Примеры

Показывает различные способы добавления полей в абзац.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Ниже приведены три способа добавления поля в конец абзаца.
// 1 — добавить поле ДАТА, используя тип поля, а затем обновить его:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 — добавить поле ВРЕМЯ, используя код поля:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 — Добавьте поле ЦИТАТЫ, используя код поля, и заставьте его отображать значение заполнителя:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// В этом поле будет отображаться значение заполнителя, пока мы его не обновим.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Смотрите также

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* пространство имен [Aspose.Words](../../paragraph/)
* сборка [Aspose.Words](../../../)



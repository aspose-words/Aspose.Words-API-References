---
title: Paragraph.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words для .NET
description: Paragraph InsertField метод. Вставляет поле в этот абзац на С#.
type: docs
weight: 270
url: /ru/net/aspose.words/paragraph/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool, [Node](../../node/), bool*) {#insertfield}

Вставляет поле в этот абзац.

```csharp
public Field InsertField(FieldType fieldType, bool updateField, Node refNode, bool isAfter)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldType | FieldType | Тип поля для вставки. |
| updateField | Boolean | Указывает, следует ли немедленно обновить поле. |
| refNode | Node | Справочный узел внутри этого абзаца (если*refNode* является`нулевой`, затем добавляется в конец абзаца). |
| isAfter | Boolean | Вставлять ли поле после или перед опорным узлом. |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field/) объект, представляющий вставленное поле.

## Примеры

Показаны различные способы добавления полей в абзац.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Ниже приведены три способа вставки поля в абзац.
// 1 — вставить поле AUTHOR в абзац после одного из дочерних узлов абзаца:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Вставьте поле ЦИТАТЫ после одного из дочерних узлов абзаца:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Вставьте поле ЦИТАТЫ перед одним из дочерних узлов абзаца,
// и заставить его отобразить значение заполнителя:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// В этом поле будет отображаться значение заполнителя, пока мы его не обновим.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Смотрите также

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Node](../../node/)
* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertField(*string, [Node](../../node/), bool*) {#insertfield_1}

Вставляет поле в этот абзац.

```csharp
public Field InsertField(string fieldCode, Node refNode, bool isAfter)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | String | Код поля для вставки (без фигурных скобок). |
| refNode | Node | Справочный узел внутри этого абзаца (если*refNode* является`нулевой`, затем добавляется в конец абзаца). |
| isAfter | Boolean | Вставлять ли поле после или перед опорным узлом. |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field/) объект, представляющий вставленное поле.

## Примеры

Показаны различные способы добавления полей в абзац.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Ниже приведены три способа вставки поля в абзац.
// 1 — вставить поле AUTHOR в абзац после одного из дочерних узлов абзаца:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Вставьте поле ЦИТАТЫ после одного из дочерних узлов абзаца:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Вставьте поле ЦИТАТЫ перед одним из дочерних узлов абзаца,
// и заставить его отобразить значение заполнителя:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// В этом поле будет отображаться значение заполнителя, пока мы его не обновим.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Смотрите также

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertField(*string, string, [Node](../../node/), bool*) {#insertfield_2}

Вставляет поле в этот абзац.

```csharp
public Field InsertField(string fieldCode, string fieldValue, Node refNode, bool isAfter)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | String | Код поля для вставки (без фигурных скобок). |
| fieldValue | String | Значение поля для вставки. Проходить`нулевой` для полей, которые не имеют значения. |
| refNode | Node | Справочный узел внутри этого абзаца (если*refNode* является`нулевой`, затем добавляется в конец абзаца). |
| isAfter | Boolean | Вставлять ли поле после или перед опорным узлом. |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field/) объект, представляющий вставленное поле.

## Примеры

Показаны различные способы добавления полей в абзац.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Ниже приведены три способа вставки поля в абзац.
// 1 — вставить поле AUTHOR в абзац после одного из дочерних узлов абзаца:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Вставьте поле ЦИТАТЫ после одного из дочерних узлов абзаца:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Вставьте поле ЦИТАТЫ перед одним из дочерних узлов абзаца,
// и заставить его отобразить значение заполнителя:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// В этом поле будет отображаться значение заполнителя, пока мы его не обновим.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Смотрите также

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

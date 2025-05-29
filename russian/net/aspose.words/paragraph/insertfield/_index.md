---
title: Paragraph.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words для .NET
description: Легко вставляйте поля в абзацы с помощью метода Paragraph InsertField. Расширьте функциональность документа и оптимизируйте управление содержимым.
type: docs
weight: 290
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
| refNode | Node | Узел ссылки внутри этого абзаца (если*refNode* является`нулевой`, затем добавляется в конец абзаца). |
| isAfter | Boolean | Вставлять ли поле после или до ссылочного узла. |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field/) объект, представляющий вставленное поле.

## Примеры

Показаны различные способы добавления полей в абзац.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Ниже приведены три способа вставки поля в абзац.
// 1 - Вставить поле AUTHOR в абзац после одного из дочерних узлов абзаца:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Вставьте поле QUOTE после одного из дочерних узлов абзаца:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Вставьте поле ЦИТАТА перед одним из дочерних узлов абзаца,
// и заставить его отображать значение-заполнитель:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Это поле будет отображать свое значение-заполнитель, пока мы его не обновим.
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
| refNode | Node | Узел ссылки внутри этого абзаца (если*refNode* является`нулевой`, затем добавляется в конец абзаца). |
| isAfter | Boolean | Вставлять ли поле после или до ссылочного узла. |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field/) объект, представляющий вставленное поле.

## Примеры

Показаны различные способы добавления полей в абзац.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Ниже приведены три способа вставки поля в абзац.
// 1 - Вставить поле AUTHOR в абзац после одного из дочерних узлов абзаца:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Вставьте поле QUOTE после одного из дочерних узлов абзаца:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Вставьте поле ЦИТАТА перед одним из дочерних узлов абзаца,
// и заставить его отображать значение-заполнитель:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Это поле будет отображать свое значение-заполнитель, пока мы его не обновим.
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
| fieldValue | String | Значение поля для вставки. Пройти`нулевой` для полей, не имеющих значения. |
| refNode | Node | Узел ссылки внутри этого абзаца (если*refNode* является`нулевой`, затем добавляется в конец абзаца). |
| isAfter | Boolean | Вставлять ли поле после или до ссылочного узла. |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field/) объект, представляющий вставленное поле.

## Примеры

Показаны различные способы добавления полей в абзац.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Ниже приведены три способа вставки поля в абзац.
// 1 - Вставить поле AUTHOR в абзац после одного из дочерних узлов абзаца:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Вставьте поле QUOTE после одного из дочерних узлов абзаца:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Вставьте поле ЦИТАТА перед одним из дочерних узлов абзаца,
// и заставить его отображать значение-заполнитель:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Это поле будет отображать свое значение-заполнитель, пока мы его не обновим.
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

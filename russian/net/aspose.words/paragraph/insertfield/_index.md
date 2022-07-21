---
title: InsertField
second_title: Справочник по API Aspose.Words для .NET
description: Вставляет поле в этот абзац.
type: docs
weight: 270
url: /ru/net/aspose.words/paragraph/insertfield/
---
## InsertField(FieldType, bool, Node, bool) {#insertfield}

Вставляет поле в этот абзац.

```csharp
public Field InsertField(FieldType fieldType, bool updateField, Node refNode, bool isAfter)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldType | FieldType | Тип поля для вставки. |
| updateField | Boolean | Указывает, следует ли обновлять поле немедленно. |
| refNode | Node | Узел ссылки внутри этого абзаца (если refNode имеет значение null, то добавляется в конец абзаца). |
| isAfter | Boolean | Следует ли вставлять поле после или перед ссылочным узлом. |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field) объект, представляющий вставленное поле.

### Примеры

Показаны различные способы добавления полей в абзац.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Ниже приведены три способа вставки поля в абзац.
// 1 - Вставьте поле AUTHOR в абзац после одного из дочерних узлов абзаца:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Вставьте поле QUOTE после одного из дочерних узлов абзаца:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Вставьте поле QUOTE перед одним из дочерних узлов абзаца,
// и заставить его отображать значение заполнителя:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// В этом поле будет отображаться значение-заполнитель, пока мы его не обновим.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Смотрите также

* class [Field](../../../aspose.words.fields/field)
* enum [FieldType](../../../aspose.words.fields/fieldtype)
* class [Node](../../node)
* class [Paragraph](../../paragraph)
* пространство имен [Aspose.Words](../../paragraph)
* сборка [Aspose.Words](../../../)

---

## InsertField(string, Node, bool) {#insertfield_1}

Вставляет поле в этот абзац.

```csharp
public Field InsertField(string fieldCode, Node refNode, bool isAfter)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | String | Код поля для вставки (без фигурных скобок). |
| refNode | Node | Узел ссылки внутри этого абзаца (если refNode имеет значение null, то добавляется в конец абзаца). |
| isAfter | Boolean | Следует ли вставлять поле после или перед ссылочным узлом. |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field) объект, представляющий вставленное поле.

### Примеры

Показаны различные способы добавления полей в абзац.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Ниже приведены три способа вставки поля в абзац.
// 1 - Вставьте поле AUTHOR в абзац после одного из дочерних узлов абзаца:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Вставьте поле QUOTE после одного из дочерних узлов абзаца:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Вставьте поле QUOTE перед одним из дочерних узлов абзаца,
// и заставить его отображать значение заполнителя:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// В этом поле будет отображаться значение-заполнитель, пока мы его не обновим.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Смотрите также

* class [Field](../../../aspose.words.fields/field)
* class [Node](../../node)
* class [Paragraph](../../paragraph)
* пространство имен [Aspose.Words](../../paragraph)
* сборка [Aspose.Words](../../../)

---

## InsertField(string, string, Node, bool) {#insertfield_2}

Вставляет поле в этот абзац.

```csharp
public Field InsertField(string fieldCode, string fieldValue, Node refNode, bool isAfter)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | String | Код поля для вставки (без фигурных скобок). |
| fieldValue | String | Значение поля для вставки. Передайте null для полей, которые не имеют значения. |
| refNode | Node | Узел ссылки внутри этого абзаца (если refNode имеет значение null, то добавляется в конец абзаца). |
| isAfter | Boolean | Следует ли вставлять поле после или перед ссылочным узлом. |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field) объект, представляющий вставленное поле.

### Примеры

Показаны различные способы добавления полей в абзац.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Ниже приведены три способа вставки поля в абзац.
// 1 - Вставьте поле AUTHOR в абзац после одного из дочерних узлов абзаца:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Вставьте поле QUOTE после одного из дочерних узлов абзаца:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Вставьте поле QUOTE перед одним из дочерних узлов абзаца,
// и заставить его отображать значение заполнителя:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// В этом поле будет отображаться значение-заполнитель, пока мы его не обновим.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Смотрите также

* class [Field](../../../aspose.words.fields/field)
* class [Node](../../node)
* class [Paragraph](../../paragraph)
* пространство имен [Aspose.Words](../../paragraph)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

---
title: DocumentBuilder.EndEditableRange
linktitle: EndEditableRange
articleTitle: EndEditableRange
second_title: Aspose.Words для .NET
description: Откройте для себя метод EndEditableRange в DocumentBuilder, который позволяет эффективно отмечать редактируемые разделы в документах, улучшая рабочий процесс редактирования.
type: docs
weight: 230
url: /ru/net/aspose.words/documentbuilder/endeditablerange/
---
## EndEditableRange() {#endeditablerange}

Отмечает текущую позицию в документе как конец редактируемого диапазона.

```csharp
public EditableRangeEnd EndEditableRange()
```

### Возвращаемое значение

Редактируемый конечный узел диапазона, который был только что создан.

## Примечания

Редактируемый диапазон в документе может перекрывать и охватывать любой диапазон. Чтобы создать допустимый редактируемый диапазон, вам нужно вызвать to оба[`StartEditableRange`](../starteditablerange/) и`EndEditableRange` или`EndEditableRange` методы.

Неправильно сформированный редактируемый диапазон будет проигнорирован при сохранении документа.

## Примеры

Показывает, как работать с редактируемым диапазоном.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// Редактируемые диапазоны позволяют нам оставлять части защищенных документов открытыми для редактирования.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// Правильно сформированный редактируемый диапазон имеет начальный узел и конечный узел.
// Эти узлы имеют совпадающие идентификаторы и включают редактируемые узлы.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Различные части редактируемого диапазона связаны друг с другом.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// Мы можем получить доступ к типам узлов каждой части следующим образом. Редактируемый диапазон сам по себе не является узлом,
// а сущность, состоящая из начала, конца и их вложенного содержимого.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Удалить редактируемый диапазон. Все узлы, которые были внутри диапазона, останутся нетронутыми.
editableRange.Remove();
```

### Смотрите также

* class [EditableRangeEnd](../../editablerangeend/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## EndEditableRange(*[EditableRangeStart](../../editablerangestart/)*) {#endeditablerange_1}

Отмечает текущую позицию в документе как конец редактируемого диапазона.

```csharp
public EditableRangeEnd EndEditableRange(EditableRangeStart start)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| start | EditableRangeStart | Это начало редактируемого диапазона. |

### Возвращаемое значение

Редактируемый конечный узел диапазона, который был только что создан.

## Примечания

Используйте эту перегрузку при создании вложенных редактируемых диапазонов.

Редактируемый диапазон в документе может перекрывать и охватывать любой диапазон. Чтобы создать допустимый редактируемый диапазон, вам нужно вызвать to оба[`StartEditableRange`](../starteditablerange/) и`EndEditableRange` или`EndEditableRange` методы.

Неправильно сформированный редактируемый диапазон будет проигнорирован при сохранении документа.

## Примеры

Показывает, как создавать вложенные редактируемые диапазоны.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.");

// Создаем два вложенных редактируемых диапазона.
EditableRangeStart outerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside the outer editable range and can be edited.");

EditableRangeStart innerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// В настоящее время курсор вставки узла конструктора документов находится более чем в одном текущем редактируемом диапазоне.
// Когда мы хотим завершить редактируемый диапазон в этой ситуации,
// нам нужно указать, какой из диапазонов мы хотим завершить, передав его узел EditableRangeStart.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// Если область текста имеет два перекрывающихся редактируемых диапазона с указанными группами,
// объединенная группа пользователей, исключенных обеими группами, не может редактировать его.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
```

### Смотрите также

* class [EditableRangeEnd](../../editablerangeend/)
* class [EditableRangeStart](../../editablerangestart/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

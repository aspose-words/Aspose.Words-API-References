---
title: EditableRangeStart.EditableRange
second_title: Справочник по API Aspose.Words для .NET
description: EditableRangeStart свойство. Получает объект фасада который инкапсулирует начало и конец этого редактируемого диапазона.
type: docs
weight: 10
url: /ru/net/aspose.words/editablerangestart/editablerange/
---
## EditableRangeStart.EditableRange property

Получает объект фасада, который инкапсулирует начало и конец этого редактируемого диапазона.

```csharp
public EditableRange EditableRange { get; }
```

### Примеры

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

// Правильно сформированный редактируемый диапазон имеет начальный и конечный узлы.
// Эти узлы имеют совпадающие идентификаторы и включают в себя редактируемые узлы.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Различные части редактируемого диапазона связаны друг с другом.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// Мы можем получить доступ к типам узлов каждой части следующим образом. Редактируемый диапазон сам по себе не является узлом.
// но сущность, состоящая из начала, конца и их содержимого.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Удалить редактируемый диапазон. Все узлы, находившиеся внутри диапазона, останутся нетронутыми.
editableRange.Remove();
```

### Смотрите также

* class [EditableRange](../../editablerange/)
* class [EditableRangeStart](../)
* пространство имен [Aspose.Words](../../editablerangestart/)
* сборка [Aspose.Words](../../../)



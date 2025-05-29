---
title: EditableRange.EditableRangeStart
linktitle: EditableRangeStart
articleTitle: EditableRangeStart
second_title: Aspose.Words для .NET
description: Откройте для себя свойство EditableRangeStart для доступа к узлу, отмечающему начало вашего редактируемого диапазона. Расширьте свой опыт редактирования сегодня!
type: docs
weight: 20
url: /ru/net/aspose.words/editablerange/editablerangestart/
---
## EditableRange.EditableRangeStart property

Получает узел, представляющий начало редактируемого диапазона.

```csharp
public EditableRangeStart EditableRangeStart { get; }
```

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

* class [EditableRangeStart](../../editablerangestart/)
* class [EditableRange](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

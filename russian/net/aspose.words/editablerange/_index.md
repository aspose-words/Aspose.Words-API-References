---
title: Class EditableRange
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.EditableRange сорт. Представляет один редактируемый диапазон.
type: docs
weight: 1270
url: /ru/net/aspose.words/editablerange/
---
## EditableRange class

Представляет один редактируемый диапазон.

```csharp
public class EditableRange
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [EditableRangeEnd](../../aspose.words/editablerange/editablerangeend/) { get; } | Получает узел, представляющий конец редактируемого диапазона. |
| [EditableRangeStart](../../aspose.words/editablerange/editablerangestart/) { get; } | Получает узел, представляющий начало редактируемого диапазона. |
| [EditorGroup](../../aspose.words/editablerange/editorgroup/) { get; set; } | Возвращает или задает псевдоним (или группу редактирования), который должен использоваться для определения того, разрешено ли текущему пользователю редактировать этот редактируемый диапазон. |
| [Id](../../aspose.words/editablerange/id/) { get; } | Получает редактируемый идентификатор диапазона. |
| [SingleUser](../../aspose.words/editablerange/singleuser/) { get; set; } | Возвращает или задает одного пользователя для редактируемого диапазона. |

## Методы

| Имя | Описание |
| --- | --- |
| [Remove](../../aspose.words/editablerange/remove/)() | Удаляет редактируемый диапазон из документа. Не удаляет содержимое внутри редактируемого диапазона. |

### Примечания

`EditableRange` это объект «фасад», который инкапсулирует два узла[`EditableRangeStart`](./editablerangestart/) и[`EditableRangeEnd`](./editablerangeend/) в дереве документа и позволяет работать с редактируемым диапазоном как с единым объектом.

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

// Правильно сформированный редактируемый диапазон имеет начальный узел и конечный узел.
// Эти узлы имеют совпадающие идентификаторы и охватывают редактируемые узлы.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Различные части редактируемого диапазона связаны друг с другом.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// Мы можем получить доступ к типам узлов каждой части следующим образом. Редактируемый диапазон сам по себе не является узлом,
// но объект, который состоит из начала, конца и заключенного в них содержимого.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Удалить редактируемый диапазон. Все узлы, которые были внутри диапазона, останутся нетронутыми.
editableRange.Remove();
```

Показывает, как ограничить права редактирования редактируемых диапазонов определенной группой/пользователем.

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // Когда мы защищаем документы от записи, редактируемые диапазоны позволяют нам выбирать определенные области, которые могут редактировать пользователи.
    // Есть два взаимоисключающих способа сузить список разрешенных редакторов.
    // 1 - Указываем пользователя:
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 - Указываем группу, с которой связаны разрешенные пользователи:
    editableRange = builder.StartEditableRange().EditableRange;
    editableRange.EditorGroup = EditorType.Administrators;
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.EditorGroup}.");
    builder.EndEditableRange();

    Assert.AreEqual(string.Empty, editableRange.SingleUser);

    builder.Writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

    // Печатаем детали и содержимое каждого редактируемого диапазона в документе.
    EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

    doc.Accept(editableRangePrinter);

    Console.WriteLine(editableRangePrinter.ToText());
}

/// <summary>
/// Собирает свойства и содержимое посещенных редактируемых диапазонов в строку.
/// </summary>
public class EditableRangePrinter : DocumentVisitor
{
    public EditableRangePrinter()
    {
        mBuilder = new StringBuilder();
    }

    public string ToText()
    {
        return mBuilder.ToString();
    }

    public void Reset()
    {
        mBuilder.Clear();
        mInsideEditableRange = false;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел EditableRangeStart.
    /// </summary>
    public override VisitorAction VisitEditableRangeStart(EditableRangeStart editableRangeStart)
    {
        mBuilder.AppendLine(" -- Editable range found! -- ");
        mBuilder.AppendLine("\tID:\t\t" + editableRangeStart.Id);
        if (editableRangeStart.EditableRange.SingleUser == string.Empty)
            mBuilder.AppendLine("\tGroup:\t" + editableRangeStart.EditableRange.EditorGroup);
        else
            mBuilder.AppendLine("\tUser:\t" + editableRangeStart.EditableRange.SingleUser);
        mBuilder.AppendLine("\tContents:");

        mInsideEditableRange = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел EditableRangeEnd.
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mBuilder.AppendLine(" -- End of editable range --\n");

        mInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел Run. Этот посетитель записывает только те пробеги, которые находятся в редактируемых диапазонах.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mInsideEditableRange) mBuilder.AppendLine("\t\"" + run.Text + "\"");

        return VisitorAction.Continue;
    }

    private bool mInsideEditableRange;
    private readonly StringBuilder mBuilder;
}
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)



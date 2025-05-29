---
title: EditableRangeEnd Class
linktitle: EditableRangeEnd
articleTitle: EditableRangeEnd
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.EditableRangeEnd, предназначенный для эффективного управления редактируемыми диапазонами в документах Word для беспрепятственного редактирования документов.
type: docs
weight: 1840
url: /ru/net/aspose.words/editablerangeend/
---
## EditableRangeEnd class

Обозначает конец редактируемого диапазона в документе Word.

Чтобы узнать больше, посетите[Объектная модель документа Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) документальная статья.

```csharp
public sealed class EditableRangeEnd : Node
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, к которому принадлежит этот узел. |
| [EditableRangeStart](../../aspose.words/editablerangeend/editablerangestart/) { get; } | Соответствующий[`EditableRangeStart`](../editablerangestart/) , получено ID. |
| [Id](../../aspose.words/editablerangeend/id/) { get; set; } | Указывает идентификатор редактируемого диапазона. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Возврат`истинный` если этот узел может содержать другие узлы. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за данным узлом. |
| override [NodeType](../../aspose.words/editablerangeend/nodetype/) { get; } | ВозвратEditableRangeEnd . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий данному узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../range/)объект, представляющий часть документа, содержащуюся в этом узле. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/editablerangeend/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Принимает посетителя. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Создает дубликат узла. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Получает первого предка указанного[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Получает первого предка указанного типа объекта. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Получает текст этого узла и всех его дочерних узлов. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родителя. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

## Примечания

Полный редактируемый диапазон в документе Word состоит из[`EditableRangeStart`](./editablerangestart/) и соответствующий`EditableRangeEnd` с тем же идентификатором.

[`EditableRangeStart`](./editablerangestart/) и`EditableRangeEnd` — это всего лишь маркеры внутри document , которые указывают, где начинается и заканчивается редактируемый диапазон.

Используйте[`EditableRange`](../editablerange/)класс как «фасад» для работы с редактируемым диапазоном как с единым объектом.

В настоящее время редактируемые диапазоны поддерживаются только на уровне inline, то есть внутри[`Paragraph`](../paragraph/), но начало редактируемого диапазона и конец редактируемого диапазона могут находиться в разных абзацах.

## Примеры

Показывает, как ограничить права редактирования редактируемых диапазонов определенной группой/пользователем.

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // Когда мы защищаем документы от записи, редактируемые диапазоны позволяют нам выбирать определенные области, которые пользователи могут редактировать.
    // Существует два взаимоисключающих способа сузить список разрешенных редакторов.
    // 1 - Укажите пользователя:
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 - Укажите группу, с которой связаны разрешенные пользователи:
    editableRange = builder.StartEditableRange().EditableRange;
    editableRange.EditorGroup = EditorType.Administrators;
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.EditorGroup}.");
    builder.EndEditableRange();

    Assert.AreEqual(string.Empty, editableRange.SingleUser);

    builder.Writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

    // Распечатать сведения и содержимое каждого редактируемого диапазона в документе.
    EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

    doc.Accept(editableRangePrinter);

    Console.WriteLine(editableRangePrinter.ToText());
}

/// <summary>
/// Собирает свойства и содержимое посещённых редактируемых диапазонов в строку.
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
    /// Вызывается, когда в документе встречается узел Run. Этот посетитель записывает только запуски, которые находятся внутри редактируемых диапазонов.
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

* class [Node](../node/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)

---
title: EditableRange.SingleUser
second_title: Справочник по API Aspose.Words для .NET
description: EditableRange свойство. Возвращает или задает одного пользователя для редактируемого диапазона.
type: docs
weight: 50
url: /ru/net/aspose.words/editablerange/singleuser/
---
## EditableRange.SingleUser property

Возвращает или задает одного пользователя для редактируемого диапазона.

```csharp
public string SingleUser { get; set; }
```

### Примечания

Этот редактор может быть сохранен в одной из следующих форм:

ДОМЕН\Имя пользователя - для пользователей, доступ которых должен быть аутентифицирован с использованием учетных данных домена текущего пользователя.

user@domain.com - для пользователей, доступ которых должен быть аутентифицирован с использованием адреса электронной почты пользователя в качестве учетных данных.

user - для пользователей, чей доступ должен быть аутентифицирован с использованием учетных данных компьютера текущего пользователя.

Один пользователь и группа редакторов не могут быть установлены одновременно для определенного редактируемого диапазона, , если один установлен, другой будет очищен.

### Примеры

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

* class [EditableRange](../)
* пространство имен [Aspose.Words](../../editablerange/)
* сборка [Aspose.Words](../../../)



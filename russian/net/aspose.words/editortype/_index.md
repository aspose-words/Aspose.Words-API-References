---
title: Enum EditorType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.EditorType перечисление. Определяет набор возможных псевдонимов или групп редактирования которые можно использовать в качестве псевдонимов чтобы определить разрешено ли текущему пользователю редактировать один диапазон  определенный редактируемым диапазоном в документе.
type: docs
weight: 1450
url: /ru/net/aspose.words/editortype/
---
## EditorType enumeration

Определяет набор возможных псевдонимов (или групп редактирования), которые можно использовать в качестве псевдонимов, чтобы определить, разрешено ли текущему пользователю редактировать один диапазон , определенный редактируемым диапазоном в документе.

```csharp
public enum EditorType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Unspecified | `0` | Означает, что тип редактора не указан. |
| Administrators | `1` | Указывает, что пользователям, связанным с группой «Администраторы», будет разрешено редактировать редактируемые диапазоны с использованием этого типа редактирования, когда включена защита документа. |
| Contributors | `2` | Указывает, что пользователям, связанным с группой «Участники», будет разрешено редактировать редактируемые диапазоны с использованием этого типа редактирования, когда включена защита документа. |
| Current | `3` | Указывает, что пользователям, связанным с текущей группой, будет разрешено редактировать редактируемые диапазоны с использованием этого типа редактирования, когда включена защита документа. |
| Editors | `4` | Указывает, что пользователям, связанным с группой «Редакторы», будет разрешено редактировать редактируемые диапазоны с использованием этого типа редактирования this , когда включена защита документа. |
| Everyone | `5` | Указывает, что всем пользователям, открывающим документ, будет разрешено редактировать редактируемые диапазоны с использованием этого типа редактирования , когда включена защита документа. |
| None | `6` | Указывает, что никому из пользователей, открывающих документ, не будет разрешено редактировать редактируемые диапазоны с использованием этого типа редактирования, когда защита документа включена. |
| Owners | `7` | Указывает, что пользователям, связанным с группой «Владельцы», будет разрешено редактировать редактируемые диапазоны с использованием этого типа редактирования , когда включена защита документа. |
| Default | `0` | То же, что иUnspecified . |

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

    // Когда мы защищаем документы от записи, редактируемые диапазоны позволяют нам выбирать определенные области, которые пользователи могут редактировать.
    // Есть два взаимоисключающих способа сузить список разрешенных редакторов.
    // 1 - Указываем пользователя:
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

    // Распечатываем детали и содержимое каждого редактируемого диапазона в документе.
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
    /// Вызывается, когда в документе встречается узел Run. Этот посетитель записывает только прогоны, находящиеся в пределах редактируемых диапазонов.
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



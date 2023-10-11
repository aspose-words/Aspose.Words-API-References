---
title: Interface INodeChangingCallback
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.INodeChangingCallback интерфейс. Реализуйте этот интерфейс если хотите получать уведомления при вставке или удалении узлов в документе.
type: docs
weight: 3200
url: /ru/net/aspose.words/inodechangingcallback/
---
## INodeChangingCallback interface

Реализуйте этот интерфейс, если хотите получать уведомления при вставке или удалении узлов в документе.

```csharp
public interface INodeChangingCallback
```

## Методы

| Имя | Описание |
| --- | --- |
| [NodeInserted](../../aspose.words/inodechangingcallback/nodeinserted/)(NodeChangingArgs) | Вызывается, когда узел, принадлежащий этому документу, был вставлен в другой узел. |
| [NodeInserting](../../aspose.words/inodechangingcallback/nodeinserting/)(NodeChangingArgs) | Вызывается непосредственно перед тем, как узел, принадлежащий этому документу, будет вставлен в другой узел. |
| [NodeRemoved](../../aspose.words/inodechangingcallback/noderemoved/)(NodeChangingArgs) | Вызывается, когда узел, принадлежащий этому документу, был удален из его родительского узла. |
| [NodeRemoving](../../aspose.words/inodechangingcallback/noderemoving/)(NodeChangingArgs) | Вызывается непосредственно перед тем, как узел, принадлежащий этому документу, будет удален из документа. |

### Примеры

Показывает, как настроить изменение узла с помощью обратного вызова.

```csharp
public void FontChangeViaCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Установите обратный вызов изменения узла в пользовательскую реализацию,
    // затем добавляем/удаляем узлы, чтобы создать журнал.
    HandleNodeChangingFontChanger callback = new HandleNodeChangingFontChanger();
    doc.NodeChangingCallback = callback;

    builder.Writeln("Hello world!");
    builder.Writeln("Hello again!");
    builder.InsertField(" HYPERLINK \"https://www.google.com/\" ");
    builder.InsertShape(ShapeType.Rectangle, 300, 300);

    doc.Range.Fields[0].Remove();

    Console.WriteLine(callback.GetLog());
}

/// <summary>
/// Регистрирует дату и время добавления и удаления каждого узла.
/// Устанавливает имя/размер пользовательского шрифта для текстового содержимого узлов запуска.
/// </summary>
public class HandleNodeChangingFontChanger : INodeChangingCallback
{
    void INodeChangingCallback.NodeInserted(NodeChangingArgs args)
    {
        mLog.AppendLine($"\tType:\t{args.Node.NodeType}");
        mLog.AppendLine($"\tHash:\t{args.Node.GetHashCode()}");

        if (args.Node.NodeType == NodeType.Run)
        {
            Aspose.Words.Font font = ((Run) args.Node).Font;
            mLog.Append($"\tFont:\tChanged from \"{font.Name}\" {font.Size}pt");

            font.Size = 24;
            font.Name = "Arial";

            mLog.AppendLine($" to \"{font.Name}\" {font.Size}pt");
            mLog.AppendLine($"\tContents:\n\t\t\"{args.Node.GetText()}\"");
        }
    }

    void INodeChangingCallback.NodeInserting(NodeChangingArgs args)
    {
        mLog.AppendLine($"\n{DateTime.Now:dd/MM/yyyy HH:mm:ss:fff}\tNode insertion:");
    }

    void INodeChangingCallback.NodeRemoved(NodeChangingArgs args)
    {
        mLog.AppendLine($"\tType:\t{args.Node.NodeType}");
        mLog.AppendLine($"\tHash code:\t{args.Node.GetHashCode()}");
    }

    void INodeChangingCallback.NodeRemoving(NodeChangingArgs args)
    {
        mLog.AppendLine($"\n{DateTime.Now:dd/MM/yyyy HH:mm:ss:fff}\tNode removal:");
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
}
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)



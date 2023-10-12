---
title: Class NodeChangingArgs
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.NodeChangingArgs сорт. Предоставляет данные для методовINodeChangingCallback интерфейс.
type: docs
weight: 4190
url: /ru/net/aspose.words/nodechangingargs/
---
## NodeChangingArgs class

Предоставляет данные для методов[`INodeChangingCallback`](../inodechangingcallback/) интерфейс.

Чтобы узнать больше, посетите[Объектная модель документа Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) статья документации.

```csharp
public class NodeChangingArgs
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Action](../../aspose.words/nodechangingargs/action/) { get; } | Получает значение, указывающее, какой тип события изменения узла происходит. |
| [NewParent](../../aspose.words/nodechangingargs/newparent/) { get; } | Получает родительский узел, который будет установлен после завершения операции. |
| [Node](../../aspose.words/nodechangingargs/node/) { get; } | Получает[`Node`](./node/) который добавляется или удаляется. |
| [OldParent](../../aspose.words/nodechangingargs/oldparent/) { get; } | Получает родительский узел до начала операции. |

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



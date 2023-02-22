---
title: DocumentBase.NodeChangingCallback
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBase свойство. Вызывается при вставке или удалении узла в документе.
type: docs
weight: 50
url: /ru/net/aspose.words/documentbase/nodechangingcallback/
---
## DocumentBase.NodeChangingCallback property

Вызывается при вставке или удалении узла в документе.

```csharp
public INodeChangingCallback NodeChangingCallback { get; set; }
```

### Примеры

Показывает, как настроить изменение узла с помощью обратного вызова.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Устанавливаем обратный вызов изменения узла на пользовательскую реализацию,
    // затем добавьте/удалите узлы, чтобы заставить его генерировать журнал.
    HandleNodeChangingFontChanger callback = new HandleNodeChangingFontChanger();
    doc.NodeChangingCallback = callback;

    builder.Writeln("Hello world!");
    builder.Writeln("Hello again!");
    builder.InsertField(" HYPERLINK \"https://www.google.com/\" ");
    builder.InsertShape(ShapeType.Rectangle, 300, 300);

    doc.Range.Fields[0].Remove();

    Console.WriteLine(callback.GetLog());

/// <summary>
/// Регистрирует дату и время каждой вставки и удаления узла.
/// Устанавливает пользовательское имя/размер шрифта для текстового содержимого узлов Run.
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

* interface [INodeChangingCallback](../../inodechangingcallback/)
* class [DocumentBase](../)
* пространство имен [Aspose.Words](../../documentbase/)
* сборка [Aspose.Words](../../../)



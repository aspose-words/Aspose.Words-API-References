---
title: Interface INodeChangingCallback
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.INodeChangingCallback koppel. Implementieren Sie diese Schnittstelle wenn Sie Benachrichtigungen erhalten möchten wenn Knoten im Dokument eingefügt oder entfernt werden.
type: docs
weight: 3000
url: /de/net/aspose.words/inodechangingcallback/
---
## INodeChangingCallback interface

Implementieren Sie diese Schnittstelle, wenn Sie Benachrichtigungen erhalten möchten, wenn Knoten im Dokument eingefügt oder entfernt werden.

```csharp
public interface INodeChangingCallback
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [NodeInserted](../../aspose.words/inodechangingcallback/nodeinserted/)(NodeChangingArgs) | Wird aufgerufen, wenn ein zu diesem Dokument gehörender Knoten in einen anderen Knoten eingefügt wurde. |
| [NodeInserting](../../aspose.words/inodechangingcallback/nodeinserting/)(NodeChangingArgs) | Wird aufgerufen, kurz bevor ein Knoten, der zu diesem Dokument gehört, in einen anderen Knoten eingefügt werden soll. |
| [NodeRemoved](../../aspose.words/inodechangingcallback/noderemoved/)(NodeChangingArgs) | Wird aufgerufen, wenn ein zu diesem Dokument gehörender Knoten von seinem übergeordneten Knoten entfernt wurde. |
| [NodeRemoving](../../aspose.words/inodechangingcallback/noderemoving/)(NodeChangingArgs) | Wird aufgerufen, kurz bevor ein zu diesem Dokument gehörender Knoten aus dem Dokument entfernt werden soll. |

### Beispiele

Zeigt, wie Sie Knotenänderungen mit einem Callback anpassen.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Setzen Sie den Callback für die Knotenänderung auf die benutzerdefinierte Implementierung,
    // dann Knoten hinzufügen/entfernen, um ein Protokoll zu generieren.
    HandleNodeChangingFontChanger callback = new HandleNodeChangingFontChanger();
    doc.NodeChangingCallback = callback;

    builder.Writeln("Hello world!");
    builder.Writeln("Hello again!");
    builder.InsertField(" HYPERLINK \"https://www.google.com/\" ");
    builder.InsertShape(ShapeType.Rectangle, 300, 300);

    doc.Range.Fields[0].Remove();

    Console.WriteLine(callback.GetLog());

/// <summary>
/// Protokolliert Datum und Uhrzeit jedes Einfügens und Entfernens von Knoten.
/// Legt einen benutzerdefinierten Schriftartnamen/-größe für den Textinhalt von Run-Knoten fest.
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

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)



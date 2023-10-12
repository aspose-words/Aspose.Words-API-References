---
title: Class NodeChangingArgs
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.NodeChangingArgs klas. Stellt Daten für Methoden des bereitINodeChangingCallback Schnittstelle.
type: docs
weight: 4190
url: /de/net/aspose.words/nodechangingargs/
---
## NodeChangingArgs class

Stellt Daten für Methoden des bereit[`INodeChangingCallback`](../inodechangingcallback/) Schnittstelle.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public class NodeChangingArgs
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Action](../../aspose.words/nodechangingargs/action/) { get; } | Ruft einen Wert ab, der angibt, welche Art von Knotenänderungsereignis auftritt. |
| [NewParent](../../aspose.words/nodechangingargs/newparent/) { get; } | Ruft den übergeordneten Knoten des Knotens ab, der nach Abschluss des Vorgangs festgelegt wird. |
| [Node](../../aspose.words/nodechangingargs/node/) { get; } | Ruft die ab[`Node`](./node/) das hinzugefügt oder entfernt wird. |
| [OldParent](../../aspose.words/nodechangingargs/oldparent/) { get; } | Ruft den übergeordneten Knoten des Knotens ab, bevor die Operation begann. |

### Beispiele

Zeigt, wie Knotenänderungen mit einem Rückruf angepasst werden.

```csharp
public void FontChangeViaCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Den Rückruf zum Ändern des Knotens auf eine benutzerdefinierte Implementierung setzen,
    // dann Knoten hinzufügen/entfernen, damit ein Protokoll generiert wird.
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
/// Protokolliert Datum und Uhrzeit des Einfügens und Entfernens jedes Knotens.
/// Legt einen benutzerdefinierten Schriftartnamen/eine benutzerdefinierte Schriftart für den Textinhalt von Run-Knoten fest.
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



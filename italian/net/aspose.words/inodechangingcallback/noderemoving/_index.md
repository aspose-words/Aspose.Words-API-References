---
title: INodeChangingCallback.NodeRemoving
linktitle: NodeRemoving
articleTitle: NodeRemoving
second_title: Aspose.Words per .NET
description: INodeChangingCallback NodeRemoving metodo. Chiamato subito prima che un nodo appartenente a questo documento stia per essere rimosso dal documento in C#.
type: docs
weight: 40
url: /it/net/aspose.words/inodechangingcallback/noderemoving/
---
## INodeChangingCallback.NodeRemoving method

Chiamato subito prima che un nodo appartenente a questo documento stia per essere rimosso dal documento.

```csharp
public void NodeRemoving(NodeChangingArgs args)
```

## Esempi

Mostra come personalizzare la modifica del nodo con un callback.

```csharp
public void FontChangeViaCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Imposta il callback che modifica il nodo sull'implementazione personalizzata,
    // quindi aggiungi/rimuovi nodi per far sì che generi un registro.
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
/// Registra la data e l'ora di ogni inserimento e rimozione di nodo.
/// Imposta un nome/dimensione del carattere personalizzato per il contenuto del testo dei nodi Esegui.
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

### Guarda anche

* class [NodeChangingArgs](../../nodechangingargs/)
* interface [INodeChangingCallback](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

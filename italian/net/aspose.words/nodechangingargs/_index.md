---
title: NodeChangingArgs Class
linktitle: NodeChangingArgs
articleTitle: NodeChangingArgs
second_title: Aspose.Words per .NET
description: Aspose.Words.NodeChangingArgs classe. Fornisce i dati per i metodi diINodeChangingCallback interfaccia in C#.
type: docs
weight: 4190
url: /it/net/aspose.words/nodechangingargs/
---
## NodeChangingArgs class

Fornisce i dati per i metodi di[`INodeChangingCallback`](../inodechangingcallback/) interfaccia.

Per saperne di più, visita il[Modello oggetto documento Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) articolo di documentazione.

```csharp
public class NodeChangingArgs
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Action](../../aspose.words/nodechangingargs/action/) { get; } | Ottiene un valore che indica il tipo di evento di modifica del nodo che si sta verificando. |
| [NewParent](../../aspose.words/nodechangingargs/newparent/) { get; } | Ottiene il nodo principale che verrà impostato al termine dell'operazione. |
| [Node](../../aspose.words/nodechangingargs/node/) { get; } | Ottiene il file[`Node`](./node/) che viene aggiunto o rimosso. |
| [OldParent](../../aspose.words/nodechangingargs/oldparent/) { get; } | Ottiene il genitore del nodo prima dell'inizio dell'operazione. |

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)

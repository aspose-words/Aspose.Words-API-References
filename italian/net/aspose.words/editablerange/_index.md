---
title: EditableRange Class
linktitle: EditableRange
articleTitle: EditableRange
second_title: Aspose.Words per .NET
description: Aspose.Words.EditableRange classe. Rappresenta un singolo intervallo modificabile in C#.
type: docs
weight: 1420
url: /it/net/aspose.words/editablerange/
---
## EditableRange class

Rappresenta un singolo intervallo modificabile.

Per saperne di più, visita il[Modello oggetto documento Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) articolo di documentazione.

```csharp
public class EditableRange
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [EditableRangeEnd](../../aspose.words/editablerange/editablerangeend/) { get; } | Ottiene il nodo che rappresenta la fine dell'intervallo modificabile. |
| [EditableRangeStart](../../aspose.words/editablerange/editablerangestart/) { get; } | Ottiene il nodo che rappresenta l'inizio dell'intervallo modificabile. |
| [EditorGroup](../../aspose.words/editablerange/editorgroup/) { get; set; } | Restituisce o imposta un alias (o gruppo di modifica) che verrà utilizzato per determinare se l'utente corrente potrà modificare questo intervallo modificabile. |
| [Id](../../aspose.words/editablerange/id/) { get; } | Ottiene l'identificatore dell'intervallo modificabile. |
| [SingleUser](../../aspose.words/editablerange/singleuser/) { get; set; } | Restituisce o imposta il singolo utente per l'intervallo modificabile. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Remove](../../aspose.words/editablerange/remove/)() | Rimuove l'intervallo modificabile dal documento. Non rimuove il contenuto all'interno dell'intervallo modificabile. |

## Osservazioni

`EditableRange` è un oggetto "facciata" che incapsula due nodi[`EditableRangeStart`](./editablerangestart/) e[`EditableRangeEnd`](./editablerangeend/) in un albero del documento e consente di lavorare con un intervallo modificabile come un singolo oggetto.

## Esempi

Mostra come lavorare con un intervallo modificabile.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// Gli intervalli modificabili ci consentono di lasciare parti di documenti protetti aperte per la modifica.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// Un intervallo modificabile ben formato ha un nodo iniziale e un nodo finale.
// Questi nodi hanno ID corrispondenti e comprendono nodi modificabili.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Parti diverse dell'intervallo modificabile si collegano tra loro.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// Possiamo accedere ai tipi di nodo di ciascuna parte in questo modo. L'intervallo modificabile in sé non è un nodo,
// ma un'entità che consiste in un inizio, una fine e il contenuto racchiuso.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Rimuove un intervallo modificabile. Tutti i nodi che erano all'interno dell'intervallo rimarranno intatti.
editableRange.Remove();
```

Mostra come limitare i diritti di modifica degli intervalli modificabili a un gruppo/utente specifico.

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // Quando proteggiamo i documenti dalla scrittura, gli intervalli modificabili ci consentono di scegliere aree specifiche che gli utenti possono modificare.
    // Esistono due modi reciprocamente esclusivi per restringere l'elenco degli editor consentiti.
    // 1 - Specifica un utente:
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 - Specificare un gruppo a cui sono associati gli utenti autorizzati:
    editableRange = builder.StartEditableRange().EditableRange;
    editableRange.EditorGroup = EditorType.Administrators;
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.EditorGroup}.");
    builder.EndEditableRange();

    Assert.AreEqual(string.Empty, editableRange.SingleUser);

    builder.Writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

    // Stampa i dettagli e il contenuto di ogni intervallo modificabile nel documento.
    EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

    doc.Accept(editableRangePrinter);

    Console.WriteLine(editableRangePrinter.ToText());
}

/// <summary>
/// Raccoglie le proprietà e il contenuto degli intervalli modificabili visitati in una stringa.
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
    /// Chiamato quando nel documento viene rilevato un nodo EditableRangeStart.
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
    /// Chiamato quando nel documento viene rilevato un nodo EditableRangeEnd.
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mBuilder.AppendLine(" -- End of editable range --\n");

        mInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene incontrato un nodo Esegui. Questo visitatore registra solo le esecuzioni che rientrano negli intervalli modificabili.
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

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)

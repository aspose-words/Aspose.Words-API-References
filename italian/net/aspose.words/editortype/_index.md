---
title: Enum EditorType
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.EditorType enum. Specifica linsieme di possibili alias o gruppi di modifica che possono essere utilizzati come alias per determinare se allutente corrente sarà consentito modificare un singolo intervallo definito da un intervallo modificabile allinterno di un documento.
type: docs
weight: 1450
url: /it/net/aspose.words/editortype/
---
## EditorType enumeration

Specifica l'insieme di possibili alias (o gruppi di modifica) che possono essere utilizzati come alias per determinare se all'utente corrente sarà consentito modificare un singolo intervallo definito da un intervallo modificabile all'interno di un documento.

```csharp
public enum EditorType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Unspecified | `0` | Significa che il tipo di editor non è specificato. |
| Administrators | `1` | Specifica che agli utenti associati al gruppo Amministratori sarà consentito modificare gli intervalli modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata. |
| Contributors | `2` | Specifica che agli utenti associati al gruppo Collaboratori sarà consentito modificare gli intervalli modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata. |
| Current | `3` | Specifica che agli utenti associati al gruppo Corrente sarà consentito modificare gli intervalli modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata. |
| Editors | `4` | Specifica che agli utenti associati al gruppo Editors sarà consentito modificare gli intervalli modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata. |
| Everyone | `5` | Specifica che a tutti gli utenti che aprono il documento sarà consentito modificare gli intervalli modificabili utilizzando questo tipo editing quando la protezione del documento è abilitata. |
| None | `6` | Specifica che a nessuno degli utenti che aprono il documento sarà consentito modificare gli intervalli modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata. |
| Owners | `7` | Specifica che agli utenti associati al gruppo Proprietari sarà consentito modificare gli intervalli modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata. |
| Default | `0` | Uguale aUnspecified . |

### Esempi

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



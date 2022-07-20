---
title: SingleUser
second_title: Aspose.Words per .NET API Reference
description: Restituisce o imposta il singolo utente per lintervallo modificabile.
type: docs
weight: 50
url: /it/net/aspose.words/editablerange/singleuser/
---
## EditableRange.SingleUser property

Restituisce o imposta il singolo utente per l'intervallo modificabile.

```csharp
public string SingleUser { get; set; }
```

### Osservazioni

Questo editor può essere archiviato in una delle seguenti forme:

DOMAIN\Username - per gli utenti il cui accesso deve essere autenticato utilizzando le credenziali di dominio dell'utente corrente.

user@domain.com - per gli utenti il cui accesso deve essere autenticato utilizzando l'indirizzo e-mail dell'utente come credenziali.

utente - per gli utenti il cui accesso deve essere autenticato utilizzando le credenziali della macchina dell'utente corrente.

Un singolo utente e un gruppo di editor non possono essere impostati contemporaneamente per l'intervallo modificabile specifico, se l'uno è impostato, l'altro sarà azzerato.

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

    // Quando proteggiamo i documenti in scrittura, gli intervalli modificabili ci consentono di selezionare aree specifiche che gli utenti possono modificare.
    // Esistono due modi che si escludono a vicenda per restringere l'elenco degli editor consentiti.
    // 1 - Specifica un utente:
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 - Specifica un gruppo a cui sono associati gli utenti autorizzati:
    editableRange = builder.StartEditableRange().EditableRange;
    editableRange.EditorGroup = EditorType.Administrators;
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.EditorGroup}.");
    builder.EndEditableRange();

    Assert.AreEqual(string.Empty, editableRange.SingleUser);

    builder.Writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

    // Stampa dettagli e contenuti di ogni intervallo modificabile nel documento.
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
    /// Chiamato quando viene rilevato un nodo EditableRangeStart nel documento.
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
    /// Chiamato quando viene rilevato un nodo EditableRangeEnd nel documento.
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mBuilder.AppendLine(" -- End of editable range --\n");

        mInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo Run nel documento. Questo visitatore registra solo le corse che si trovano all'interno di intervalli modificabili.
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

* class [EditableRange](../../editablerange)
* spazio dei nomi [Aspose.Words](../../editablerange)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

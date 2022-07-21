---
title: EditorGroup
second_title: Aspose.Words per .NET API Reference
description: Restituisce o imposta un alias o gruppo di modifica che deve essere utilizzato per determinare se lutente corrente può modificare questo intervallo modificabile.
type: docs
weight: 30
url: /it/net/aspose.words/editablerange/editorgroup/
---
## EditableRange.EditorGroup property

Restituisce o imposta un alias (o gruppo di modifica) che deve essere utilizzato per determinare se l'utente corrente può modificare questo intervallo modificabile.

```csharp
public EditorType EditorGroup { get; set; }
```

### Osservazioni

Non è possibile impostare contemporaneamente un singolo utente e un gruppo di editor per l'intervallo modificabile specifico, se l'uno è impostato, l'altro sarà azzerato.

### Esempi

Mostra come creare intervalli modificabili nidificati.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.");

// Crea due intervalli modificabili nidificati.
EditableRangeStart outerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside the outer editable range and can be edited.");

EditableRangeStart innerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// Attualmente, il cursore di inserimento del nodo del generatore di documenti si trova in più di un intervallo modificabile in corso.
// Quando vogliamo terminare un intervallo modificabile in questa situazione,
// dobbiamo specificare quale degli intervalli vogliamo terminare passando il suo nodo EditableRangeStart.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// Se un'area di testo ha due intervalli modificabili sovrapposti con gruppi specificati,
// al gruppo combinato di utenti esclusi da entrambi i gruppi viene impedito di modificarlo.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
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

* enum [EditorType](../../editortype)
* class [EditableRange](../../editablerange)
* spazio dei nomi [Aspose.Words](../../editablerange)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

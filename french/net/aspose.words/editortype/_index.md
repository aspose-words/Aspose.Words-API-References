---
title: EditorType
second_title: Référence de l'API Aspose.Words pour .NET
description: Spécifie lensemble des alias possibles ou groupes dédition qui peuvent être utilisés comme alias pour déterminer si lutilisateur actuel doit être autorisé à modifier une seule plage définie par une plage modifiable dans un document.
type: docs
weight: 1300
url: /fr/net/aspose.words/editortype/
---
## EditorType enumeration

Spécifie l'ensemble des alias possibles (ou groupes d'édition) qui peuvent être utilisés comme alias pour déterminer si l'utilisateur actuel doit être autorisé à modifier une seule plage définie par une plage modifiable dans un document.

```csharp
public enum EditorType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Unspecified | `0` | Signifie que le type d'éditeur n'est pas spécifié. |
| Administrators | `1` | Spécifie que les utilisateurs associés au groupe Administrateurs doivent être autorisés à modifier les plages modifiables en utilisant ce type de modification lorsque la protection des documents est activée. |
| Contributors | `2` | Spécifie que les utilisateurs associés au groupe Contributors doivent être autorisés à modifier les plages modifiables en utilisant ce type de modification lorsque la protection des documents est activée. |
| Current | `3` | Spécifie que les utilisateurs associés au groupe Actuel doivent être autorisés à modifier les plages modifiables à l'aide de ce type de modification lorsque la protection des documents est activée. |
| Editors | `4` | Spécifie que les utilisateurs associés au groupe Éditeurs doivent être autorisés à modifier les plages modifiables à l'aide de ce type de modification lorsque la protection des documents est activée. |
| Everyone | `5` | Spécifie que tous les utilisateurs qui ouvrent le document doivent être autorisés à modifier les plages modifiables à l'aide de ce type d'édition lorsque la protection du document est activée. |
| None | `6` | Spécifie qu'aucun des utilisateurs qui ouvrent le document ne sera autorisé à modifier les plages modifiables à l'aide de ce type de modification lorsque la protection du document est activée. |
| Owners | `7` | Spécifie que les utilisateurs associés au groupe Propriétaires doivent être autorisés à modifier les plages modifiables à l'aide de ce type de modification lorsque la protection des documents est activée. |
| Default | `0` | Identique àUnspecified . |

### Exemples

Montre comment limiter les droits de modification des plages modifiables à un groupe/utilisateur spécifique.

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // Lorsque nous protégeons des documents en écriture, les plages modifiables nous permettent de sélectionner des zones spécifiques que les utilisateurs peuvent modifier.
    // Il existe deux manières mutuellement exclusives de réduire la liste des éditeurs autorisés.
    // 1 - Spécifiez un utilisateur :
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 - Spécifiez un groupe auquel les utilisateurs autorisés sont associés :
    editableRange = builder.StartEditableRange().EditableRange;
    editableRange.EditorGroup = EditorType.Administrators;
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.EditorGroup}.");
    builder.EndEditableRange();

    Assert.AreEqual(string.Empty, editableRange.SingleUser);

    builder.Writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

    // Affiche les détails et le contenu de chaque plage modifiable du document.
    EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

    doc.Accept(editableRangePrinter);

    Console.WriteLine(editableRangePrinter.ToText());
}

/// <summary>
/// Collecte les propriétés et le contenu des plages modifiables visitées dans une chaîne.
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
    /// Appelé lorsqu'un nœud EditableRangeStart est rencontré dans le document.
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
    /// Appelé lorsqu'un nœud EditableRangeEnd est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mBuilder.AppendLine(" -- End of editable range --\n");

        mInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un noeud Run est rencontré dans le document. Ce visiteur n'enregistre que les exécutions qui se trouvent dans des plages modifiables.
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

### Voir également

* espace de noms [Aspose.Words](../../aspose.words)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

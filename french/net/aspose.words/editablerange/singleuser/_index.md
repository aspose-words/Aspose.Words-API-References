---
title: EditableRange.SingleUser
linktitle: SingleUser
articleTitle: SingleUser
second_title: Aspose.Words pour .NET
description: EditableRange SingleUser propriété. Renvoie ou définit lutilisateur unique pour la plage modifiable en C#.
type: docs
weight: 50
url: /fr/net/aspose.words/editablerange/singleuser/
---
## EditableRange.SingleUser property

Renvoie ou définit l'utilisateur unique pour la plage modifiable.

```csharp
public string SingleUser { get; set; }
```

## Remarques

Cet éditeur peut être stocké sous l'une des formes suivantes :

DOMAIN\Username - pour les utilisateurs dont l'accès doit être authentifié à l'aide des informations d'identification de domaine de l'utilisateur actuel.

user@domain.com - pour les utilisateurs dont l'accès doit être authentifié en utilisant l'adresse e-mail de l'utilisateur comme identifiant.

utilisateur - pour les utilisateurs dont l'accès doit être authentifié à l'aide des informations d'identification de la machine de l'utilisateur actuel.

Un seul utilisateur et un groupe d'éditeurs ne peuvent pas être définis simultanément pour la plage modifiable spécifique, si l'un est défini, l'autre sera clair.

## Exemples

Montre comment limiter les droits d'édition des plages modifiables à un groupe/utilisateur spécifique.

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

    // Imprimer les détails et le contenu de chaque plage modifiable du document.
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
    /// Appelé lorsqu'un nœud Run est rencontré dans le document. Ce visiteur enregistre uniquement les exécutions situées dans des plages modifiables.
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

* class [EditableRange](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

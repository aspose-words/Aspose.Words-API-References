---
title: EditableRange Class
linktitle: EditableRange
articleTitle: EditableRange
second_title: Aspose.Words pour .NET
description: Aspose.Words.EditableRange classe. Représente une seule plage modifiable en C#.
type: docs
weight: 1420
url: /fr/net/aspose.words/editablerange/
---
## EditableRange class

Représente une seule plage modifiable.

Pour en savoir plus, visitez le[Modèle objet de document (DOM) Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) article documentaire.

```csharp
public class EditableRange
```

## Propriétés

| Nom | La description |
| --- | --- |
| [EditableRangeEnd](../../aspose.words/editablerange/editablerangeend/) { get; } | Obtient le nœud qui représente la fin de la plage modifiable. |
| [EditableRangeStart](../../aspose.words/editablerange/editablerangestart/) { get; } | Obtient le nœud qui représente le début de la plage modifiable. |
| [EditorGroup](../../aspose.words/editablerange/editorgroup/) { get; set; } | Renvoie ou définit un alias (ou un groupe d'édition) qui doit être utilisé pour déterminer si l'utilisateur actuel doit être autorisé à modifier cette plage modifiable. |
| [Id](../../aspose.words/editablerange/id/) { get; } | Obtient l'identifiant de plage modifiable. |
| [SingleUser](../../aspose.words/editablerange/singleuser/) { get; set; } | Renvoie ou définit l'utilisateur unique pour la plage modifiable. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Remove](../../aspose.words/editablerange/remove/)() | Supprime la plage modifiable du document. Ne supprime pas le contenu à l'intérieur de la plage modifiable. |

## Remarques

`EditableRange` est un objet "façade" qui encapsule deux nœuds[`EditableRangeStart`](./editablerangestart/) et[`EditableRangeEnd`](./editablerangeend/) dans une arborescence de documents et permet de travailler avec une plage modifiable comme un objet unique.

## Exemples

Montre comment travailler avec une plage modifiable.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// Les plages modifiables nous permettent de laisser des parties de documents protégés ouvertes pour l'édition.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// Une plage modifiable bien formée a un nœud de début et un nœud de fin.
// Ces nœuds ont des ID correspondants et englobent des nœuds modifiables.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Différentes parties de la plage modifiable sont liées les unes aux autres.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// Nous pouvons accéder aux types de nœuds de chaque partie comme ceci. La plage modifiable elle-même n'est pas un nœud,
// mais une entité composée d'un début, d'une fin et de leur contenu inclus.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Supprime une plage modifiable. Tous les nœuds qui se trouvaient à l'intérieur de la plage resteront intacts.
editableRange.Remove();
```

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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)

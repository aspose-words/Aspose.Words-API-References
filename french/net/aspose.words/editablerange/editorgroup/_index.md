---
title: EditableRange.EditorGroup
linktitle: EditorGroup
articleTitle: EditorGroup
second_title: Aspose.Words pour .NET
description: Gérez les autorisations des utilisateurs sans effort avec la propriété EditableRange EditorGroup, permettant de contrôler l'accès à l'édition pour une collaboration améliorée.
type: docs
weight: 30
url: /fr/net/aspose.words/editablerange/editorgroup/
---
## EditableRange.EditorGroup property

Renvoie ou définit un alias (ou un groupe d'édition) qui doit être utilisé pour déterminer si l'utilisateur actuel doit être autorisé à modifier cette plage modifiable.

```csharp
public EditorType EditorGroup { get; set; }
```

## Remarques

Un seul utilisateur et un groupe d'éditeurs ne peuvent pas être définis simultanément pour la plage modifiable spécifique, si l'un est défini, l'autre sera effacé.

## Exemples

Montre comment créer des plages modifiables imbriquées.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.");

// Créez deux plages modifiables imbriquées.
EditableRangeStart outerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside the outer editable range and can be edited.");

EditableRangeStart innerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// Actuellement, le curseur d'insertion de nœud du générateur de documents se trouve dans plusieurs plages modifiables en cours.
// Lorsque nous voulons terminer une plage modifiable dans cette situation,
// nous devons spécifier laquelle des plages nous souhaitons terminer en passant son nœud EditableRangeStart.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// Si une région de texte comporte deux plages modifiables qui se chevauchent avec des groupes spécifiés,
// le groupe combiné d'utilisateurs exclus par les deux groupes ne peut pas le modifier.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
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

    // Imprimez les détails et le contenu de chaque plage modifiable dans le document.
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
    /// Appelé lorsqu'un nœud Run est rencontré dans le document. Ce visiteur enregistre uniquement les exécutions comprises dans des plages modifiables.
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

* enum [EditorType](../../editortype/)
* class [EditableRange](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

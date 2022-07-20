---
title: Hidden
second_title: Référence de l'API Aspose.Words pour .NET
description: Vrai si la police est formatée en tant que texte masqué.
type: docs
weight: 140
url: /fr/net/aspose.words/font/hidden/
---
## Font.Hidden property

Vrai si la police est formatée en tant que texte masqué.

```csharp
public bool Hidden { get; set; }
```

### Exemples

Montre comment créer une série de texte masqué.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Avec l'indicateur Hidden défini sur true, tout texte que nous créons à l'aide de cet objet Font sera invisible dans le document.
// Nous ne verrons ni ne mettrons en surbrillance le texte masqué à moins d'activer l'option "Texte masqué"
// trouvé dans Microsoft Word via "Fichier" -> "Options" -> "Affichage". Le texte sera toujours là,
// et nous pourrons accéder à ce texte par programmation.
// Il est déconseillé d'utiliser cette méthode pour masquer des informations sensibles.
builder.Font.Hidden = true;
builder.Font.Size = 36;

builder.Writeln("This text will not be visible in the document.");

doc.Save(ArtifactsDir + "Font.Hidden.docx");
```

Montre comment utiliser une implémentation DocumentVisitor pour supprimer tout le contenu masqué d'un document.

```csharp
{
    Document doc = new Document(MyDir + "Hidden content.docx");

    RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

    // Ci-dessous trois types de champs pouvant accepter un visiteur de document,
    // qui lui permettra de visiter le nœud acceptant, puis de parcourir ses nœuds enfants en profondeur d'abord.
    // 1 - Nœud Paragraphe :
    Paragraph para = (Paragraph) doc.GetChild(NodeType.Paragraph, 4, true);
    para.Accept(hiddenContentRemover);

    // 2 - Noeud Table :
    Table table = doc.FirstSection.Body.Tables[0];
    table.Accept(hiddenContentRemover);

    // 3 - Noeud document :
    doc.Accept(hiddenContentRemover);

    doc.Save(ArtifactsDir + "Font.RemoveHiddenContentFromDocument.docx");

/// <summary>
/// Supprime tous les nœuds visités marqués comme "contenu caché".
/// </summary>
public class RemoveHiddenContentVisitor : DocumentVisitor
{
    /// <summary>
    /// Appelé lorsqu'un nœud FieldStart est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        if (fieldStart.Font.Hidden)
            fieldStart.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud FieldEnd est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.Font.Hidden)
            fieldEnd.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud FieldSeparator est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        if (fieldSeparator.Font.Hidden)
            fieldSeparator.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un noeud Run est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (run.Font.Hidden)
            run.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud Paragraphe est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        if (paragraph.ParagraphBreakFont.Hidden)
            paragraph.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un FormField est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitFormField(FormField formField)
    {
        if (formField.Font.Hidden)
            formField.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un GroupShape est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        if (groupShape.Font.Hidden)
            groupShape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un Shape est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitShapeStart(Shape shape)
    {
        if (shape.Font.Hidden)
            shape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un commentaire est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitCommentStart(Comment comment)
    {
        if (comment.Font.Hidden)
            comment.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'une note de bas de page est rencontrée dans le document.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        if (footnote.Font.Hidden)
            footnote.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un SpecialCharacter est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitSpecialChar(SpecialChar specialChar)
    {
        if (specialChar.Font.Hidden)
            specialChar.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsque la visite d'un nœud Table est terminée dans le document.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        // Le contenu à l'intérieur des cellules du tableau peut avoir l'indicateur de contenu masqué, mais les tableaux eux-mêmes ne le peuvent pas.
        // Si ce tableau n'avait que du contenu caché, ce visiteur l'aurait tout supprimé,
        // et il n'y aurait plus de nœuds enfants.
        // Ainsi, nous pouvons également traiter le tableau lui-même comme un contenu caché et le supprimer.
        // Les tableaux qui sont vides mais qui n'ont pas de contenu caché auront des cellules avec des paragraphes vides à l'intérieur,
        // que ce visiteur ne supprimera pas.
        if (!table.HasChildNodes)
            table.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsque la visite d'un noeud Cellule est terminée dans le document.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        if (!cell.HasChildNodes && cell.ParentNode != null)
            cell.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsque la visite d'un nœud Row est terminée dans le document.
    /// </summary>
    public override VisitorAction VisitRowEnd(Row row)
    {
        if (!row.HasChildNodes && row.ParentNode != null)
            row.Remove();

        return VisitorAction.Continue;
    }
}
```

### Voir également

* class [Font](../../font)
* espace de noms [Aspose.Words](../../font)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

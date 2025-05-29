---
title: DocumentVisitor.VisitCommentRangeStart
linktitle: VisitCommentRangeStart
articleTitle: VisitCommentRangeStart
second_title: Aspose.Words pour .NET
description: Explorez la méthode DocumentVisitor VisitCommentRangeStart pour gérer efficacement les commentaires de texte dans votre code, améliorant ainsi la lisibilité et l'organisation.
type: docs
weight: 120
url: /fr/net/aspose.words/documentvisitor/visitcommentrangestart/
---
## DocumentVisitor.VisitCommentRangeStart method

Appelé lorsque le début d'une plage de texte commentée est rencontré.

```csharp
public virtual VisitorAction VisitCommentRangeStart(CommentRangeStart commentRangeStart)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| commentRangeStart | CommentRangeStart | L'objet qui est visité. |

### Return_Value

UN[`VisitorAction`](../../visitoraction/) valeur qui spécifie comment continuer l'énumération.

## Exemples

Montre comment imprimer la structure des nœuds de chaque commentaire et plage de commentaires dans un document.

```csharp
public void CommentsToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    CommentStructurePrinter visitor = new CommentStructurePrinter();

    // Lorsque nous obtenons un nœud composite pour accepter un visiteur de document, le visiteur visite le nœud acceptant,
    // et parcourt ensuite tous les enfants du nœud de manière approfondie.
    // Le visiteur peut lire et modifier chaque nœud visité.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Parcourt l'arbre non binaire des nœuds enfants d'un nœud.
/// Crée une carte sous la forme d'une chaîne de tous les nœuds Comment/CommentRange rencontrés et de leurs enfants.
/// </summary>
public class CommentStructurePrinter : DocumentVisitor
{
    public CommentStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideComment = false;
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Appelé lorsqu'un nœud Run est rencontré dans le document.
    /// Une exécution n'est enregistrée que si elle est un enfant d'un nœud Comment ou CommentRange.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud CommentRangeStart est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitCommentRangeStart(CommentRangeStart commentRangeStart)
    {
        IndentAndAppendLine("[Comment range start] ID: " + commentRangeStart.Id);
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud CommentRangeEnd est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment range end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud Comment est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitCommentStart(Comment comment)
    {
        IndentAndAppendLine(
            $"[Comment start] For comment range ID {comment.Id}, By {comment.Author} on {comment.DateTime}");
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé après que tous les nœuds enfants d'un nœud Commentaire ont été visités.
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Ajoutez une ligne au StringBuilder et indentez-la en fonction de la profondeur du visiteur
    /// dans l'arbre de nœuds enfants d'un commentaire/d'une plage de commentaires.
    /// </summary>
    /// <param name="texte"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++)
        {
            mBuilder.Append("|  ");
        }

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideComment;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Voir également

* enum [VisitorAction](../../visitoraction/)
* class [CommentRangeStart](../../commentrangestart/)
* class [DocumentVisitor](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

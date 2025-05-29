---
title: CommentRangeEnd.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Id CommentRangeEnd, qui relie vos commentaires de manière transparente. Optimisez la gestion de votre contenu grâce à cet identifiant essentiel pour une meilleure organisation.
type: docs
weight: 20
url: /fr/net/aspose.words/commentrangeend/id/
---
## CommentRangeEnd.Id property

Spécifie l'identifiant du commentaire auquel cette région est liée.

```csharp
public int Id { get; set; }
```

## Exemples

Montre comment imprimer le contenu de tous les commentaires et leurs plages de commentaires à l'aide d'un visiteur de document.

```csharp
public void CreateCommentsAndPrintAllInfo()
{
    Document doc = new Document();

    Comment newComment = new Comment(doc)
    {
        Author = "VDeryushev",
        Initial = "VD",
        DateTime = DateTime.Now
    };

    newComment.SetText("Comment regarding text.");

    // Ajoutez du texte au document, déformez-le dans une plage de commentaires, puis ajoutez votre commentaire.
    Paragraph para = doc.FirstSection.Body.FirstParagraph;
    para.AppendChild(new CommentRangeStart(doc, newComment.Id));
    para.AppendChild(new Run(doc, "Commented text."));
    para.AppendChild(new CommentRangeEnd(doc, newComment.Id));
    para.AppendChild(newComment); 

    // Ajoutez deux réponses au commentaire.
    newComment.AddReply("John Doe", "JD", DateTime.Now, "New reply.");
    newComment.AddReply("John Doe", "JD", DateTime.Now, "Another reply.");

    PrintAllCommentInfo(doc.GetChildNodes(NodeType.Comment, true));
}

/// <summary>
/// Itère sur chaque commentaire de niveau supérieur et imprime sa plage de commentaires, son contenu et ses réponses.
/// </summary>
private static void PrintAllCommentInfo(NodeCollection comments)
{
    CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

    // Itérer sur tous les commentaires de niveau supérieur. Contrairement aux commentaires de type réponse, les commentaires de niveau supérieur n'ont pas d'ancêtre.
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null).ToList())
    {
        // Tout d’abord, visitez le début de la plage de commentaires.
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // Ensuite, visitez le commentaire et toutes les réponses qu'il peut contenir.
        comment.Accept(commentVisitor);
        // Visitez uniquement le début du commentaire.
        comment.AcceptStart(commentVisitor);
        // Visitez uniquement la fin du commentaire.
        comment.AcceptEnd(commentVisitor);

        foreach (Comment reply in comment.Replies)
            reply.Accept(commentVisitor);

        // Enfin, visitez la fin de la plage de commentaires, puis imprimez le contenu du texte du visiteur.
        CommentRangeEnd commentRangeEnd = (CommentRangeEnd)comment.PreviousSibling;
        commentRangeEnd.Accept(commentVisitor);

        Console.WriteLine(commentVisitor.GetText());
    }
}

/// <summary>
/// Imprime les informations et le contenu de tous les commentaires et plages de commentaires rencontrés dans le document.
/// </summary>
public class CommentInfoPrinter : DocumentVisitor
{
    public CommentInfoPrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideComment = false;
    }

    /// <summary>
    /// Obtient le texte brut du document accumulé par le visiteur.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Appelé lorsqu'un nœud Run est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.Text + "\"");

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
        IndentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.Id + "\n");
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
    /// Appelé lorsque la visite d'un nœud Commentaire est terminée dans le document.
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Ajoutez une ligne au StringBuilder et indentez-la en fonction de la profondeur à laquelle se trouve le visiteur dans l'arborescence du document.
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

* class [CommentRangeEnd](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

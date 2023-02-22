---
title: Class CommentRangeEnd
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.CommentRangeEnd classe. Indique la fin dune zone de texte à laquelle un commentaire est associé.
type: docs
weight: 240
url: /fr/net/aspose.words/commentrangeend/
---
## CommentRangeEnd class

Indique la fin d'une zone de texte à laquelle un commentaire est associé.

```csharp
public sealed class CommentRangeEnd : Node
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [CommentRangeEnd](commentrangeend/)(DocumentBase, int) | Initialise une nouvelle instance de cette classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel ce nœud appartient. |
| [Id](../../aspose.words/commentrangeend/id/) { get; set; } | Spécifie l'identifiant du commentaire auquel cette région est liée. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Renvoie true si ce nœud peut contenir d'autres nœuds. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words/commentrangeend/nodetype/) { get; } | RetoursCommentRangeEnd . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words/commentrangeend/accept/)(DocumentVisitor) | Accepte un visiteur. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un doublon du nœud. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Obtient le texte de ce nœud et de tous ses enfants. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-ordre. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options d'enregistrement spécifiées. |

### Remarques

Pour créer un commentaire ancré à une zone de texte, vous devez créer un[`Comment`](../comment/) and puis créer[`CommentRangeStart`](../commentrangestart/) et`CommentRangeEnd`et définissez leurs identifiants sur le même[`Id`](../comment/id/) évaluer.

`CommentRangeEnd` est un nœud de niveau en ligne et ne peut être qu'un enfant de[`Paragraph`](../paragraph/).

### Exemples

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

    // Ajoute deux réponses au commentaire.
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

    // Itération sur tous les commentaires de niveau supérieur. Contrairement aux commentaires de type réponse, les commentaires de niveau supérieur n'ont pas d'ancêtre.
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null))
    {
        // Tout d'abord, visitez le début de la plage de commentaires.
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // Ensuite, visitez le commentaire et toutes les réponses qu'il peut avoir.
        comment.Accept(commentVisitor);

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
    /// Obtient le texte brut du document qui a été accumulé par le visiteur.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Appelé lorsqu'un noeud Run est rencontré dans le document.
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
    /// Appelé lorsqu'un nœud Commentaire est rencontré dans le document.
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
    /// Ajoutez une ligne au StringBuilder et indentez-la en fonction de la profondeur du visiteur dans l'arborescence du document.
    /// </summary>
    /// <nom du paramètre="texte"></param>
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

* class [Node](../node/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)



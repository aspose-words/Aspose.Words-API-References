---
title: Footnote.AcceptStart
linktitle: AcceptStart
articleTitle: AcceptStart
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Footnote AcceptStart, conçue pour améliorer l'engagement des visiteurs en guidant de manière transparente les utilisateurs vers le début de la note de bas de page.
type: docs
weight: 100
url: /fr/net/aspose.words.notes/footnote/acceptstart/
---
## Footnote.AcceptStart method

Accepte un visiteur pour visiter le début de la note de bas de page.

```csharp
public override VisitorAction AcceptStart(DocumentVisitor visitor)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| visitor | DocumentVisitor | Le visiteur du document. |

### Return_Value

L'action à entreprendre par le visiteur.

## Exemples

Montre comment imprimer la structure des nœuds de chaque note de bas de page dans un document.

```csharp
public void FootnoteToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FootnoteStructurePrinter visitor = new FootnoteStructurePrinter();

    // Lorsque nous obtenons un nœud composite pour accepter un visiteur de document, le visiteur visite le nœud acceptant,
    // et parcourt ensuite tous les enfants du nœud de manière approfondie.
    // Le visiteur peut lire et modifier chaque nœud visité.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Parcourt l'arbre non binaire des nœuds enfants d'un nœud.
/// Crée une carte sous la forme d'une chaîne de tous les nœuds Footnote rencontrés et de leurs enfants.
/// </summary>
public class FootnoteStructurePrinter : DocumentVisitor
{
    public FootnoteStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideFootnote = false;
    }

    /// <summary>
    /// Obtient le texte brut du document accumulé par le visiteur.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Appelé lorsqu'un nœud Footnote est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        IndentAndAppendLine("[Footnote start] Type: " + footnote.FootnoteType);
        mDocTraversalDepth++;
        mVisitorIsInsideFootnote = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé après que tous les nœuds enfants d'un nœud Footnote ont été visités.
    /// </summary>
    public override VisitorAction VisitFootnoteEnd(Footnote footnote)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Footnote end]");
        mVisitorIsInsideFootnote = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud Run est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideFootnote) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Ajoutez une ligne au StringBuilder et indentez-la en fonction de la profondeur à laquelle se trouve le visiteur dans l'arborescence du document.
    /// </summary>
    /// <param name="texte"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideFootnote;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Voir également

* enum [VisitorAction](../../../aspose.words/visitoraction/)
* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [Footnote](../)
* espace de noms [Aspose.Words.Notes](../../../aspose.words.notes/)
* Assemblée [Aspose.Words](../../../)

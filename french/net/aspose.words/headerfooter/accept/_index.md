---
title: HeaderFooter.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words pour .NET
description: Découvrez la méthode HeaderFooter Accept pour améliorer l'engagement des visiteurs et rationaliser les interactions sur votre site Web sans effort.
type: docs
weight: 70
url: /fr/net/aspose.words/headerfooter/accept/
---
## HeaderFooter.Accept method

Accepte un visiteur.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| visitor | DocumentVisitor | Le visiteur qui visitera les nœuds. |

### Return_Value

Vrai si tous les nœuds ont été visités ; faux si[`DocumentVisitor`](../../documentvisitor/) a arrêté l'opération avant de visiter tous les nœuds.

## Remarques

Énumère ce nœud et tous ses enfants. Chaque nœud appelle une méthode correspondante sur[`DocumentVisitor`](../../documentvisitor/).

Pour plus d'informations, consultez le modèle de conception Visitor.

Appels[`VisitHeaderFooterStart`](../../documentvisitor/visitheaderfooterstart/) , puis appelle[`Accept`](../../node/accept/) pour tous les nœuds enfants de la section et les appels[`VisitHeaderFooterEnd`](../../documentvisitor/visitheaderfooterend/) à la fin.

## Exemples

Montre comment imprimer la structure des nœuds de chaque en-tête et pied de page d'un document.

```csharp
public void HeaderFooterToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    HeaderFooterStructurePrinter visitor = new HeaderFooterStructurePrinter();

    // Lorsque nous obtenons un nœud composite pour accepter un visiteur de document, le visiteur visite le nœud acceptant,
    // et parcourt ensuite tous les enfants du nœud de manière approfondie.
    // Le visiteur peut lire et modifier chaque nœud visité.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // Une autre façon d'accéder section par section à l'en-tête/pied de page d'un document est d'accéder à la collection.
    HeaderFooter[] headerFooters = doc.FirstSection.HeadersFooters.ToArray();
    Assert.AreEqual(3, headerFooters.Length);
}

/// <summary>
/// Parcourt l'arbre non binaire des nœuds enfants d'un nœud.
/// Crée une carte sous la forme d'une chaîne de tous les nœuds HeaderFooter rencontrés et de leurs enfants.
/// </summary>
public class HeaderFooterStructurePrinter : DocumentVisitor
{
    public HeaderFooterStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideHeaderFooter = false;
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Appelé lorsqu'un nœud Run est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideHeaderFooter) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud HeaderFooter est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitHeaderFooterStart(HeaderFooter headerFooter)
    {
        IndentAndAppendLine("[HeaderFooter start] HeaderFooterType: " + headerFooter.HeaderFooterType);
        mDocTraversalDepth++;
        mVisitorIsInsideHeaderFooter = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé après que tous les nœuds enfants d'un nœud HeaderFooter ont été visités.
    /// </summary>
    public override VisitorAction VisitHeaderFooterEnd(HeaderFooter headerFooter)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[HeaderFooter end]");
        mVisitorIsInsideHeaderFooter = false;

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

    private bool mVisitorIsInsideHeaderFooter;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Voir également

* class [DocumentVisitor](../../documentvisitor/)
* class [HeaderFooter](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

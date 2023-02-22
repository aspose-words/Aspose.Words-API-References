---
title: SubDocument.Accept
second_title: Référence de l'API Aspose.Words pour .NET
description: SubDocument méthode. Accepte un visiteur.
type: docs
weight: 20
url: /fr/net/aspose.words/subdocument/accept/
---
## SubDocument.Accept method

Accepte un visiteur.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| visitor | DocumentVisitor | Le visiteur qui visitera les nœuds. |

### Return_Value

Vrai si tous les nœuds ont été visités ; false si DocumentVisitor a arrêté l'opération avant de visiter tous les nœuds.

### Remarques

Énumère ce nœud et tous ses enfants. Chaque nœud appelle une méthode correspondante sur DocumentVisitor.

Pour plus d'informations, consultez le modèle de conception Visiteur.

### Exemples

Montre comment utiliser un visiteur de document pour imprimer la structure de nœud d'un document.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // Lorsque nous obtenons un nœud composite pour accepter un visiteur de document, le visiteur visite le nœud acceptant,
    // puis parcourt tous les enfants du nœud en profondeur d'abord.
    // Le visiteur peut lire et modifier chaque nœud visité.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Parcourt l'arborescence des nœuds enfants d'un nœud.
/// Crée une carte de cet arbre sous la forme d'une chaîne.
/// </summary>
public class DocStructurePrinter : DocumentVisitor
{
    public DocStructurePrinter()
    {
        mAcceptingNodeChildTree = new StringBuilder();
    }

    public string GetText()
    {
        return mAcceptingNodeChildTree.ToString();
    }

    /// <summary>
    /// Appelé lorsqu'un nœud Document est rencontré.
    /// </summary>
    public override VisitorAction VisitDocumentStart(Document doc)
    {
        int childNodeCount = doc.GetChildNodes(NodeType.Any, true).Count;

        IndentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
        mDocTraversalDepth++;

        // Autoriser le visiteur à continuer à visiter d'autres nœuds.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé après que tous les nœuds enfants d'un nœud Document ont été visités.
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud Section est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
        // Récupère l'index de notre section dans le document.
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé après que tous les nœuds enfants d'un nœud Section ont été visités.
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud Body est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé après que tous les nœuds enfants d'un nœud Body ont été visités.
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud Paragraphe est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé après que tous les nœuds enfants d'un nœud Paragraphe ont été visités.
    /// </summary>
    public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Paragraph end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un noeud Run est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud SubDocument est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Ajoutez une ligne au StringBuilder et indentez-la en fonction de la profondeur du visiteur dans l'arborescence du document.
    /// </summary>
    /// <nom du paramètre="texte"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mAcceptingNodeChildTree.Append("|  ");

        mAcceptingNodeChildTree.AppendLine(text);
    }

    private int mDocTraversalDepth;
    private readonly StringBuilder mAcceptingNodeChildTree;
}
```

### Voir également

* class [DocumentVisitor](../../documentvisitor/)
* class [SubDocument](../)
* espace de noms [Aspose.Words](../../subdocument/)
* Assemblée [Aspose.Words](../../../)



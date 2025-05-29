---
title: DocumentVisitor.VisitStructuredDocumentTagEnd
linktitle: VisitStructuredDocumentTagEnd
articleTitle: VisitStructuredDocumentTagEnd
second_title: Aspose.Words pour .NET
description: Découvrez la méthode DocumentVisitor VisitStructuredDocumentTagEnd, essentielle pour gérer efficacement l'énumération des balises de documents structurés. Améliorez vos compétences en codage !
type: docs
weight: 440
url: /fr/net/aspose.words/documentvisitor/visitstructureddocumenttagend/
---
## DocumentVisitor.VisitStructuredDocumentTagEnd method

Appelé lorsque l'énumération d'une balise de document structuré est terminée.

```csharp
public virtual VisitorAction VisitStructuredDocumentTagEnd(StructuredDocumentTag sdt)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| sdt | StructuredDocumentTag | L'objet qui est visité. |

### Return_Value

UN[`VisitorAction`](../../visitoraction/) valeur qui spécifie comment continuer l'énumération.

## Exemples

Montre comment imprimer la structure du nœud de chaque balise de document structuré dans un document.

```csharp
public void StructuredDocumentTagToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    StructuredDocumentTagNodePrinter visitor = new StructuredDocumentTagNodePrinter();

    // Lorsque nous obtenons un nœud composite pour accepter un visiteur de document, le visiteur visite le nœud acceptant,
    // et parcourt ensuite tous les enfants du nœud de manière approfondie.
    // Le visiteur peut lire et modifier chaque nœud visité.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Parcourt l'arbre non binaire des nœuds enfants d'un nœud.
/// Crée une carte sous la forme d'une chaîne de tous les nœuds StructuredDocumentTag rencontrés et de leurs enfants.
/// </summary>
public class StructuredDocumentTagNodePrinter : DocumentVisitor
{
    public StructuredDocumentTagNodePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideStructuredDocumentTag = false;
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
        if (mVisitorIsInsideStructuredDocumentTag) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud StructuredDocumentTag est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagStart(StructuredDocumentTag sdt)
    {
        IndentAndAppendLine("[StructuredDocumentTag start] Title: " + sdt.Title);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé après que tous les nœuds enfants d'un nœud StructuredDocumentTag ont été visités.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagEnd(StructuredDocumentTag sdt)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[StructuredDocumentTag end]");

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

    private readonly bool mVisitorIsInsideStructuredDocumentTag;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Voir également

* enum [VisitorAction](../../visitoraction/)
* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentVisitor](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

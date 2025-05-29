---
title: DocumentVisitor.VisitSmartTagEnd
linktitle: VisitSmartTagEnd
articleTitle: VisitSmartTagEnd
second_title: Aspose.Words pour .NET
description: Découvrez la méthode DocumentVisitor VisitSmartTagEnd, essentielle pour une énumération efficace des balises intelligentes. Améliorez votre code grâce à cette fonctionnalité clé !
type: docs
weight: 410
url: /fr/net/aspose.words/documentvisitor/visitsmarttagend/
---
## DocumentVisitor.VisitSmartTagEnd method

Appelé lorsque l'énumération d'une balise intelligente est terminée.

```csharp
public virtual VisitorAction VisitSmartTagEnd(SmartTag smartTag)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| smartTag | SmartTag | L'objet qui est visité. |

### Return_Value

UN[`VisitorAction`](../../visitoraction/) valeur qui spécifie comment continuer l'énumération.

## Exemples

Montre comment imprimer la structure des nœuds de chaque balise intelligente dans un document.

```csharp
public void SmartTagToText()
{
    Document doc = new Document(MyDir + "Smart tags.doc");
    SmartTagStructurePrinter visitor = new SmartTagStructurePrinter();

    // Lorsque nous obtenons un nœud composite pour accepter un visiteur de document, le visiteur visite le nœud acceptant,
    // et parcourt ensuite tous les enfants du nœud de manière approfondie.
    // Le visiteur peut lire et modifier chaque nœud visité.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Parcourt l'arbre non binaire des nœuds enfants d'un nœud.
/// Crée une carte sous la forme d'une chaîne de tous les nœuds SmartTag rencontrés et de leurs enfants.
/// </summary>
public class SmartTagStructurePrinter : DocumentVisitor
{
    public SmartTagStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideSmartTag = false;
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
        if (mVisitorIsInsideSmartTag) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud SmartTag est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        IndentAndAppendLine("[SmartTag start] Name: " + smartTag.Element);
        mDocTraversalDepth++;
        mVisitorIsInsideSmartTag = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé après que tous les nœuds enfants d'un nœud SmartTag ont été visités.
    /// </summary>
    public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[SmartTag end]");
        mVisitorIsInsideSmartTag = false;

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

    private bool mVisitorIsInsideSmartTag;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Voir également

* enum [VisitorAction](../../visitoraction/)
* class [SmartTag](../../../aspose.words.markup/smarttag/)
* class [DocumentVisitor](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

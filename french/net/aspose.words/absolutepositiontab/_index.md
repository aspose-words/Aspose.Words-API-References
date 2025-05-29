---
title: AbsolutePositionTab Class
linktitle: AbsolutePositionTab
articleTitle: AbsolutePositionTab
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.AbsolutePositionTab, permettant un positionnement précis du texte dans WordprocessingML pour un formatage et un contrôle améliorés des documents.
type: docs
weight: 120
url: /fr/net/aspose.words/absolutepositiontab/
---
## AbsolutePositionTab class

Une tabulation de position absolue est un caractère utilisé pour avancer la position sur la ligne de texte actuelle lors de l'affichage de ce contenu WordprocessingML.

Pour en savoir plus, visitez le[Modèle d'objet de document (DOM) Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) article de documentation.

```csharp
public class AbsolutePositionTab : SpecialChar
```

## Propriétés

| Nom | La description |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel appartient ce nœud. |
| [Font](../../aspose.words/inline/font/) { get; } | Donne accès à la mise en forme de la police de cet objet. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Retours`vrai` si ce nœud peut contenir d'autres nœuds. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Renvoie vrai si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Renvoie true si la mise en forme de l'objet a été modifiée dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Renvoie vrai si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Retours`vrai` si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Retours`vrai` si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words/specialchar/nodetype/) { get; } | RetoursSpecialChar . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Récupère le parent[`Paragraph`](../paragraph/) de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un[`Range`](../range/)objet qui représente la partie d'un document contenue dans ce nœud. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words/absolutepositiontab/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accepte un visiteur. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crée un doublon du nœud. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Obtient le premier ancêtre du spécifié[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtient le premier ancêtre du type d'objet spécifié. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Obtient le caractère spécial que ce nœud représente. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Obtient le nœud suivant selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporte le contenu du nœud dans une chaîne en utilisant les options de sauvegarde spécifiées. |

## Exemples

Montre comment traiter les caractères de tabulation de position absolue avec un visiteur de document.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // Extraire le contenu textuel de notre document en acceptant ce visiteur de document personnalisé.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    Section fisrtSection = doc.FirstSection;
    fisrtSection.Body.Accept(myDocTextExtractor);
    // Visitez uniquement le début du corps du document.
    fisrtSection.Body.AcceptStart(myDocTextExtractor);
    // Visitez uniquement la fin du corps du document.
    fisrtSection.Body.AcceptEnd(myDocTextExtractor);

    // La position absolue tab, qui n'a pas d'équivalent sous forme de chaîne, a été explicitement convertie en caractère de tabulation.
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // Un AbsolutePositionTab peut également accepter un DocumentVisitor par lui-même.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
/// Collecte le contenu textuel de toutes les exécutions du document visité. Remplace tous les caractères de tabulation absolus par des tabulations ordinaires.
/// </summary>
public class DocTextExtractor : DocumentVisitor
{
    public DocTextExtractor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Appelé lorsqu'un nœud Run est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        AppendText(run.Text);
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud AbsolutePositionTab est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Ajoute du texte à la sortie actuelle. Respecte l'indicateur de sortie activé/désactivé.
    /// </summary>
    private void AppendText(string text)
    {
        mBuilder.Append(text);
    }

    /// <summary>
    /// Texte brut du document accumulé par le visiteur.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### Voir également

* class [SpecialChar](../specialchar/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)

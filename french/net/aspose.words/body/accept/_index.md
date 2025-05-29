---
title: Body.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Body Accept pour un engagement fluide des visiteurs. Améliorez l'expérience utilisateur et boostez vos conversions grâce à notre approche unique !
type: docs
weight: 40
url: /fr/net/aspose.words/body/accept/
---
## Body.Accept method

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

Appels[`VisitBodyStart`](../../documentvisitor/visitbodystart/) , puis appelle[`Accept`](../../node/accept/) pour tous les nœuds enfants de la section et les appels[`VisitBodyEnd`](../../documentvisitor/visitbodyend/) à la fin.

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

* class [DocumentVisitor](../../documentvisitor/)
* class [Body](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

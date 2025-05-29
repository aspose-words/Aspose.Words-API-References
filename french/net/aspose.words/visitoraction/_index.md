---
title: VisitorAction Enum
linktitle: VisitorAction
articleTitle: VisitorAction
second_title: Aspose.Words pour .NET
description: Explorez l'énumération Aspose.Words.VisitorAction pour gérer sans effort l'énumération des nœuds, améliorant ainsi l'efficacité et le contrôle du traitement de vos documents.
type: docs
weight: 7470
url: /fr/net/aspose.words/visitoraction/
---
## VisitorAction enumeration

Permet au visiteur de contrôler l'énumération des nœuds.

```csharp
public enum VisitorAction
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Continue | `0` | Le visiteur demande que l'énumération continue. |
| SkipThisNode | `1` | Le visiteur demande d'ignorer le nœud actuel et de continuer l'énumération. |
| Stop | `2` | Le visiteur demande l'arrêt de l'énumération des nœuds. |

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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)

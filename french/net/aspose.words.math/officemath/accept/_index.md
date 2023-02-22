---
title: OfficeMath.Accept
second_title: Référence de l'API Aspose.Words pour .NET
description: OfficeMath méthode. Accepte un visiteur.
type: docs
weight: 70
url: /fr/net/aspose.words.math/officemath/accept/
---
## OfficeMath.Accept method

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

Appels[`VisitOfficeMathStart`](../../../aspose.words/documentvisitor/visitofficemathstart/) , puis appelle[`Accept`](../../../aspose.words/node/accept/) pour tous nœuds enfants de Office Math et appels[`VisitOfficeMathEnd`](../../../aspose.words/documentvisitor/visitofficemathend/) à la fin.

### Exemples

Montre comment imprimer la structure de nœud de chaque nœud mathématique de bureau dans un document.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // Lorsque nous obtenons un nœud composite pour accepter un visiteur de document, le visiteur visite le nœud acceptant,
    // puis parcourt tous les enfants du nœud en profondeur d'abord.
    // Le visiteur peut lire et modifier chaque nœud visité.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Parcourt l'arborescence non binaire des nœuds enfants d'un nœud.
/// Crée une carte sous la forme d'une chaîne de tous les nœuds OfficeMath rencontrés et de leurs enfants.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
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
        if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud OfficeMath est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
    {
        IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.MathObjectType);
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé après que tous les nœuds enfants d'un nœud OfficeMath ont été visités.
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Ajoutez une ligne au StringBuilder et indentez-la en fonction de la profondeur du visiteur dans l'arborescence du document.
    /// </summary>
    /// <nom du paramètre="texte"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideOfficeMath;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Voir également

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [OfficeMath](../)
* espace de noms [Aspose.Words.Math](../../officemath/)
* Assemblée [Aspose.Words](../../../)



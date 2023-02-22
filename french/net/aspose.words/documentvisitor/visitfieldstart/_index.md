---
title: DocumentVisitor.VisitFieldStart
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentVisitor méthode. Appelé lorsquun champ commence dans le document.
type: docs
weight: 200
url: /fr/net/aspose.words/documentvisitor/visitfieldstart/
---
## DocumentVisitor.VisitFieldStart method

Appelé lorsqu'un champ commence dans le document.

```csharp
public virtual VisitorAction VisitFieldStart(FieldStart fieldStart)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldStart | FieldStart | L'objet visité. |

### Return_Value

UN[`VisitorAction`](../../visitoraction/) valeur qui spécifie comment poursuivre l'énumération.

### Remarques

Un champ dans un document Word se compose d'un code de champ et d'une valeur de champ.

Par exemple, un champ qui affiche un numéro de page peut être représenté comme suit :

[FieldStart]PAGE[FieldSeparator]98[FieldEnd]

Le séparateur de champ sépare le code de champ de la valeur de champ dans le document. Notez que certains champs n'ont qu'un code de champ et n'ont pas de séparateur de champ ni de valeur de champ.

Les champs peuvent être imbriqués.

### Exemples

Montre comment imprimer la structure de nœud de chaque champ dans un document.

```csharp
public void FieldToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FieldStructurePrinter visitor = new FieldStructurePrinter();

    // Lorsque nous obtenons un nœud composite pour accepter un visiteur de document, le visiteur visite le nœud acceptant,
    // puis parcourt tous les enfants du nœud en profondeur d'abord.
    // Le visiteur peut lire et modifier chaque nœud visité.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Parcourt l'arborescence non binaire des nœuds enfants d'un nœud.
/// Crée une carte sous la forme d'une chaîne de tous les nœuds Field rencontrés et de leurs enfants.
/// </summary>
public class FieldStructurePrinter : DocumentVisitor
{
    public FieldStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideField = false;
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Appelé lorsqu'un noeud Run est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideField) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud FieldStart est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        IndentAndAppendLine("[Field start] FieldType: " + fieldStart.FieldType);
        mDocTraversalDepth++;
        mVisitorIsInsideField = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud FieldEnd est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Field end]");
        mVisitorIsInsideField = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud FieldSeparator est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        IndentAndAppendLine("[FieldSeparator]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Ajoutez une ligne au StringBuilder et indentez-la en fonction de la profondeur du visiteur
    /// dans l'arborescence des nœuds enfants du champ.
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

    private bool mVisitorIsInsideField;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Voir également

* enum [VisitorAction](../../visitoraction/)
* class [FieldStart](../../../aspose.words.fields/fieldstart/)
* class [DocumentVisitor](../)
* espace de noms [Aspose.Words](../../documentvisitor/)
* Assemblée [Aspose.Words](../../../)



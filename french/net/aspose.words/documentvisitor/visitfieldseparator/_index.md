---
title: DocumentVisitor.VisitFieldSeparator
linktitle: VisitFieldSeparator
articleTitle: VisitFieldSeparator
second_title: Aspose.Words pour .NET
description: Découvrez la méthode VisitFieldSeparator dans DocumentVisitor. Gérez efficacement les séparateurs de champs dans vos documents pour un traitement simplifié.
type: docs
weight: 190
url: /fr/net/aspose.words/documentvisitor/visitfieldseparator/
---
## DocumentVisitor.VisitFieldSeparator method

Appelé lorsqu'un séparateur de champ est rencontré dans le document.

```csharp
public virtual VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldSeparator | FieldSeparator | L'objet qui est visité. |

### Return_Value

UN[`VisitorAction`](../../visitoraction/) valeur qui spécifie comment continuer l'énumération.

## Remarques

Le séparateur de champ sépare le code de la valeur du champ dans le document. Notez que certains champs ne contiennent que le code, sans séparateur ni valeur.

Pour plus d'informations, voir[`VisitFieldStart`](../visitfieldstart/)

## Exemples

Montre comment imprimer la structure des nœuds de chaque champ d'un document.

```csharp
public void FieldToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FieldStructurePrinter visitor = new FieldStructurePrinter();

    // Lorsque nous obtenons un nœud composite pour accepter un visiteur de document, le visiteur visite le nœud acceptant,
    // et parcourt ensuite tous les enfants du nœud de manière approfondie.
    // Le visiteur peut lire et modifier chaque nœud visité.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Parcourt l'arbre non binaire des nœuds enfants d'un nœud.
/// Crée une carte sous la forme d'une chaîne de tous les nœuds de champ rencontrés et de leurs enfants.
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
    /// Appelé lorsqu'un nœud Run est rencontré dans le document.
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
    /// <param name="texte"></param>
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
* class [FieldSeparator](../../../aspose.words.fields/fieldseparator/)
* class [DocumentVisitor](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

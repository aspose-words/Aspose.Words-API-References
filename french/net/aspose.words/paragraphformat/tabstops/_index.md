---
title: ParagraphFormat.TabStops
linktitle: TabStops
articleTitle: TabStops
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ParagraphFormat TabStops pour gérer facilement les taquets de tabulation personnalisés, améliorant ainsi la mise en forme de votre document et améliorant la lisibilité.
type: docs
weight: 400
url: /fr/net/aspose.words/paragraphformat/tabstops/
---
## ParagraphFormat.TabStops property

Obtient la collection de taquets de tabulation personnalisés définis pour cet objet.

```csharp
public TabStopCollection TabStops { get; }
```

## Exemples

Montre comment modifier la position de la tabulation droite dans les paragraphes liés à la table des matières.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Parcourez tous les paragraphes avec des styles basés sur les résultats de la table des matières ; il s'agit de n'importe quel style entre TOC et TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Obtenez le premier onglet utilisé dans ce paragraphe, cela devrait être l'onglet utilisé pour aligner les numéros de page.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Remplacez le premier taquet de tabulation par défaut par un taquet de tabulation personnalisé.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Voir également

* class [TabStopCollection](../../tabstopcollection/)
* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

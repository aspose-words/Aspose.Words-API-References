---
title: TabStop.Leader
linktitle: Leader
articleTitle: Leader
second_title: Aspose.Words pour .NET
description: Découvrez les propriétés TabStop Leader pour personnaliser les types de lignes de repère de vos onglets et améliorer la clarté et la présentation de vos documents. Optimisez votre mise en forme dès aujourd'hui !
type: docs
weight: 40
url: /fr/net/aspose.words/tabstop/leader/
---
## TabStop.Leader property

Obtient ou définit le type de la ligne de repère affichée sous le caractère de tabulation.

```csharp
public TabLeader Leader { get; set; }
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

* enum [TabLeader](../../tableader/)
* class [TabStop](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

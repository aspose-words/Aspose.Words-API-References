---
title: TabStop.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words pour .NET
description: Découvrez la propriété d'alignement TabStop pour personnaliser facilement l'alignement du texte aux taquets de tabulation, améliorant ainsi la mise en page et la lisibilité de votre document.
type: docs
weight: 20
url: /fr/net/aspose.words/tabstop/alignment/
---
## TabStop.Alignment property

Obtient ou définit l'alignement du texte à ce taquet de tabulation.

```csharp
public TabAlignment Alignment { get; set; }
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

* enum [TabAlignment](../../tabalignment/)
* class [TabStop](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

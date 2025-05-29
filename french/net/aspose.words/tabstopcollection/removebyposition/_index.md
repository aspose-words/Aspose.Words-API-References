---
title: TabStopCollection.RemoveByPosition
linktitle: RemoveByPosition
articleTitle: RemoveByPosition
second_title: Aspose.Words pour .NET
description: Supprimez facilement les taquets de tabulation de votre collection grâce à la méthode RemoveByPosition. Simplifiez la mise en forme pour un meilleur contrôle de vos documents !
type: docs
weight: 120
url: /fr/net/aspose.words/tabstopcollection/removebyposition/
---
## TabStopCollection.RemoveByPosition method

Supprime un taquet de tabulation à la position spécifiée de la collection.

```csharp
public void RemoveByPosition(double position)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| position | Double | La position (en points) de la tabulation à supprimer. |

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

* class [TabStopCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---
title: StyleCollection.ClearQuickStyleGallery
linktitle: ClearQuickStyleGallery
articleTitle: ClearQuickStyleGallery
second_title: Aspose.Words pour .NET
description: StyleCollection ClearQuickStyleGallery méthode. Supprime tous les styles du panneau Galerie de styles rapides en C#.
type: docs
weight: 80
url: /fr/net/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection.ClearQuickStyleGallery method

Supprime tous les styles du panneau Galerie de styles rapides.

```csharp
public void ClearQuickStyleGallery()
```

## Exemples

Montre comment supprimer des styles du panneau Galerie de styles.

```csharp
Document doc = new Document();
// Notez que les styles de suppression ne fonctionnent pour l'instant qu'avec le format DOCX.
doc.Styles.ClearQuickStyleGallery();

doc.Save(ArtifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### Voir également

* class [StyleCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

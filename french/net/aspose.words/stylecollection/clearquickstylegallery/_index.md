---
title: StyleCollection.ClearQuickStyleGallery
second_title: Référence de l'API Aspose.Words pour .NET
description: StyleCollection méthode. Supprime tous les styles du panneau Galerie de styles rapides.
type: docs
weight: 80
url: /fr/net/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection.ClearQuickStyleGallery method

Supprime tous les styles du panneau Galerie de styles rapides.

```csharp
public void ClearQuickStyleGallery()
```

### Exemples

Montre comment supprimer des styles du panneau Galerie de styles.

```csharp
Document doc = new Document();

// Notez que supprimer les styles ne fonctionne qu'avec le format DOCX pour l'instant.
doc.Styles.ClearQuickStyleGallery();

doc.Save(ArtifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### Voir également

* class [StyleCollection](../)
* espace de noms [Aspose.Words](../../stylecollection/)
* Assemblée [Aspose.Words](../../../)



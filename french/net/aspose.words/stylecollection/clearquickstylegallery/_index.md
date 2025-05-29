---
title: StyleCollection.ClearQuickStyleGallery
linktitle: ClearQuickStyleGallery
articleTitle: ClearQuickStyleGallery
second_title: Aspose.Words pour .NET
description: Supprimez facilement les styles de votre galerie de styles rapides grâce à la méthode ClearQuickStyleGallery de StyleCollection. Simplifiez votre processus de création dès aujourd'hui !
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
// Notez que la suppression des styles ne fonctionne qu'avec le format DOCX pour le moment.
doc.Styles.ClearQuickStyleGallery();

doc.Save(ArtifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### Voir également

* class [StyleCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

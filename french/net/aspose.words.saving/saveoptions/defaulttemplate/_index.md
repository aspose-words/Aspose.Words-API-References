---
title: SaveOptions.DefaultTemplate
linktitle: DefaultTemplate
articleTitle: DefaultTemplate
second_title: Aspose.Words pour .NET
description: Gérez vos options d'enregistrement en toute simplicité ! Définissez ou obtenez le chemin et le nom de fichier par défaut du modèle pour un traitement simplifié des documents. Optimisez votre flux de travail dès aujourd'hui !
type: docs
weight: 40
url: /fr/net/aspose.words.saving/saveoptions/defaulttemplate/
---
## SaveOptions.DefaultTemplate property

Obtient ou définit le chemin d'accès au modèle par défaut (y compris le nom de fichier). La valeur par défaut de cette propriété est**chaîne vide** (Empty ).

```csharp
public string DefaultTemplate { get; set; }
```

## Remarques

Si spécifié, ce chemin est utilisé pour charger le modèle lorsque[`AutomaticallyUpdateStyles`](../../../aspose.words/document/automaticallyupdatestyles/) est`vrai` , mais[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) est vide.

## Exemples

Montre comment définir un modèle par défaut pour les documents qui n'ont pas de modèles joints.

```csharp
Document doc = new Document();

// Activez la mise à jour automatique du style, mais ne joignez pas de document modèle.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Comme il n'y a pas de document modèle, le document n'avait aucun endroit pour suivre les modifications de style.
// Utilisez un objet SaveOptions pour définir automatiquement un modèle
// si un document que nous sauvegardons n'en a pas.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)

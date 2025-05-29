---
title: Document.AttachedTemplate
linktitle: AttachedTemplate
articleTitle: AttachedTemplate
second_title: Aspose.Words pour .NET
description: Découvrez comment gérer efficacement votre propriété Document AttachedTemplate. Définissez ou récupérez facilement le chemin complet du modèle de votre document pour une intégration fluide.
type: docs
weight: 20
url: /fr/net/aspose.words/document/attachedtemplate/
---
## Document.AttachedTemplate property

Obtient ou définit le chemin complet du modèle attaché au document.

```csharp
public string AttachedTemplate { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentNullException | Lance si vous essayez de définir un`nul` valeur. |

## Remarques

Une chaîne vide signifie que le document est attaché au modèle Normal.

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

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

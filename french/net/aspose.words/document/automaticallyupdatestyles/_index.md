---
title: Document.AutomaticallyUpdateStyles
linktitle: AutomaticallyUpdateStyles
articleTitle: AutomaticallyUpdateStyles
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété AutomaticallyUpdateStyles dans MS Word garantit que les styles de votre document se synchronisent avec le modèle à chaque fois que vous l'ouvrez, améliorant ainsi la cohérence.
type: docs
weight: 30
url: /fr/net/aspose.words/document/automaticallyupdatestyles/
---
## Document.AutomaticallyUpdateStyles property

Obtient ou définit un indicateur indiquant si les styles du document sont mis à jour pour correspondre aux styles du modèle joint chaque fois que le document est ouvert dans MS Word.

```csharp
public bool AutomaticallyUpdateStyles { get; set; }
```

## Exemples

Montre comment joindre un modèle à un document.

```csharp
Document doc = new Document();

// Les documents Microsoft Word sont livrés par défaut avec un modèle joint appelé « Normal.dotm ».
// Il n'existe pas de modèle par défaut pour les documents Aspose.Words vierges.
Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Attachez un modèle, puis définissez l'indicateur pour appliquer les modifications de style
// dans le modèle aux styles de notre document.
doc.AttachedTemplate = MyDir + "Business brochure.dotx";
doc.AutomaticallyUpdateStyles = true;

doc.Save(ArtifactsDir + "Document.AutomaticallyUpdateStyles.docx");
```

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

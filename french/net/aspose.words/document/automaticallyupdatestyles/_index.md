---
title: Document.AutomaticallyUpdateStyles
linktitle: AutomaticallyUpdateStyles
articleTitle: AutomaticallyUpdateStyles
second_title: Aspose.Words pour .NET
description: Document AutomaticallyUpdateStyles propriété. Obtient ou définit un indicateur indiquant si les styles du document sont mis à jour pour correspondre aux styles du modèle joint à chaque fois que le document est ouvert dans MS Word en C#.
type: docs
weight: 30
url: /fr/net/aspose.words/document/automaticallyupdatestyles/
---
## Document.AutomaticallyUpdateStyles property

Obtient ou définit un indicateur indiquant si les styles du document sont mis à jour pour correspondre aux styles du modèle joint à chaque fois que le document est ouvert dans MS Word.

```csharp
public bool AutomaticallyUpdateStyles { get; set; }
```

## Exemples

Montre comment joindre un modèle à un document.

```csharp
Document doc = new Document();

// Les documents Microsoft Word sont livrés par défaut avec un modèle joint appelé "Normal.dotm".
// Il n'existe pas de modèle par défaut pour les documents Aspose.Words vierges.
Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Attachez un modèle, puis définissez l'indicateur pour appliquer les modifications de style
// dans le modèle aux styles de notre document.
doc.AttachedTemplate = MyDir + "Business brochure.dotx";
doc.AutomaticallyUpdateStyles = true;

doc.Save(ArtifactsDir + "Document.AutomaticallyUpdateStyles.docx");
```

Montre comment définir un modèle par défaut pour les documents auxquels aucun modèle n'est joint.

```csharp
Document doc = new Document();

// Active la mise à jour automatique du style, mais ne joint pas de document modèle.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Puisqu'il n'y a pas de modèle de document, le document n'avait nulle part où suivre les changements de style.
// Utiliser un objet SaveOptions pour définir automatiquement un modèle
// si un document que nous enregistrons n'en possède pas.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

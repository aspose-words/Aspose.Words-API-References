---
title: SaveOptions.DefaultTemplate
linktitle: DefaultTemplate
articleTitle: DefaultTemplate
second_title: Aspose.Words pour .NET
description: SaveOptions DefaultTemplate propriété. Obtient ou définit le chemin daccès au modèle par défaut y compris le nom de fichier. La valeur par défaut de cette propriété estchaîne vide Empty en C#.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/saveoptions/defaulttemplate/
---
## SaveOptions.DefaultTemplate property

Obtient ou définit le chemin d'accès au modèle par défaut (y compris le nom de fichier). La valeur par défaut de cette propriété est**chaîne vide** (Empty).

```csharp
public string DefaultTemplate { get; set; }
```

## Remarques

S'il est spécifié, ce chemin est utilisé pour charger le modèle lorsque[`AutomaticallyUpdateStyles`](../../../aspose.words/document/automaticallyupdatestyles/) est`vrai` , mais[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) est vide.

## Exemples

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

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)

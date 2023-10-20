---
title: Document.AttachedTemplate
linktitle: AttachedTemplate
articleTitle: AttachedTemplate
second_title: Aspose.Words pour .NET
description: Document AttachedTemplate propriété. Obtient ou définit le chemin complet du modèle joint au document en C#.
type: docs
weight: 20
url: /fr/net/aspose.words/document/attachedtemplate/
---
## Document.AttachedTemplate property

Obtient ou définit le chemin complet du modèle joint au document.

```csharp
public string AttachedTemplate { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentNullException | Lance si vous essayez de régler sur un`nul` valeur. |

## Remarques

Une chaîne vide signifie que le document est joint au modèle Normal.

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

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

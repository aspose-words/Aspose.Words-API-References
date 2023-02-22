---
title: SaveOptions.CreateSaveOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: SaveOptions méthode. Crée un objet doptions denregistrement dune classe adaptée au format denregistrement spécifié.
type: docs
weight: 10
url: /fr/net/aspose.words.saving/saveoptions/createsaveoptions/
---
## CreateSaveOptions(SaveFormat) {#createsaveoptions}

Crée un objet d'options d'enregistrement d'une classe adaptée au format d'enregistrement spécifié.

```csharp
public static SaveOptions CreateSaveOptions(SaveFormat saveFormat)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| saveFormat | SaveFormat | Le format d'enregistrement pour lequel créer un objet d'options d'enregistrement. |

### Return_Value

Un objet d'une classe qui dérive de[`SaveOptions`](../).

### Exemples

Affiche une option pour optimiser la consommation de mémoire lors du rendu de documents volumineux au format PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Définissez la propriété "MemoryOptimization" sur "true" pour réduire l'empreinte mémoire des opérations d'enregistrement de documents volumineux
// au prix d'une augmentation de la durée de l'opération.
// Définissez la propriété "MemoryOptimization" sur "false" pour enregistrer normalement le document au format PDF.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../saveoptions/)
* Assemblée [Aspose.Words](../../../)

---

## CreateSaveOptions(string) {#createsaveoptions_1}

Crée un objet d'options de sauvegarde d'une classe adaptée à l'extension de fichier spécifiée dans le nom de fichier donné.

```csharp
public static SaveOptions CreateSaveOptions(string fileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | L'extension de ce nom de fichier détermine la classe de l'objet d'options de sauvegarde à créer. |

### Return_Value

Un objet d'une classe qui dérive de[`SaveOptions`](../).

### Exemples

Montre comment définir un modèle par défaut pour les documents qui n'ont pas de modèles joints.

```csharp
Document doc = new Document();

// Activer la mise à jour automatique du style, mais ne pas joindre de modèle de document.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Puisqu'il n'y a pas de modèle de document, le document n'avait nulle part où suivre les changements de style.
// Utiliser un objet SaveOptions pour définir automatiquement un modèle
// si un document que nous enregistrons n'en a pas.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../saveoptions/)
* Assemblée [Aspose.Words](../../../)



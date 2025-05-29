---
title: DocSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété SaveFormat de DocSaveOptions pour choisir facilement entre les formats Doc et Dot et enregistrer vos documents en toute simplicité. Optimisez votre flux de travail dès aujourd'hui !
type: docs
weight: 50
url: /fr/net/aspose.words.saving/docsaveoptions/saveformat/
---
## DocSaveOptions.SaveFormat property

Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Peut êtreDoc ouDot .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Exemples

Montre comment définir les options d’enregistrement pour les anciens formats Microsoft Word.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Définissez un mot de passe qui protégera le chargement du document par Microsoft Word ou Aspose.Words.
// Notez que cela ne crypte en aucune façon le contenu du document.
options.Password = "MyPassword";

// Si le document contient un bordereau d'acheminement, nous pouvons le conserver lors de l'enregistrement en définissant cet indicateur sur true.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// Pour pouvoir charger le document,
// nous devrons appliquer le mot de passe que nous avons spécifié dans l'objet DocSaveOptions dans un objet LoadOptions.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [DocSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)

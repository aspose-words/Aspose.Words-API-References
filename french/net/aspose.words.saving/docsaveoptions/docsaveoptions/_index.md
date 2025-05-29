---
title: DocSaveOptions
linktitle: DocSaveOptions
articleTitle: DocSaveOptions
second_title: Aspose.Words pour .NET
description: Découvrez le constructeur DocSaveOptions pour un enregistrement fluide de vos documents au format Doc. Améliorez votre flux de travail grâce à une gestion documentaire simple et efficace.
type: docs
weight: 10
url: /fr/net/aspose.words.saving/docsaveoptions/docsaveoptions/
---
## DocSaveOptions() {#constructor}

Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leDoc format.

```csharp
public DocSaveOptions()
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

* class [DocSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)

---

## DocSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leDoc ou Dot format.

```csharp
public DocSaveOptions(SaveFormat saveFormat)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| saveFormat | SaveFormat | Peut êtreDoc ouDot. |

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

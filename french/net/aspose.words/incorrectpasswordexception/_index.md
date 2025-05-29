---
title: IncorrectPasswordException Class
linktitle: IncorrectPasswordException
articleTitle: IncorrectPasswordException
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.IncorrectPasswordException, qui gère les erreurs de mot de passe pour les documents cryptés, garantissant un accès sécurisé et transparent.
type: docs
weight: 3700
url: /fr/net/aspose.words/incorrectpasswordexception/
---
## IncorrectPasswordException class

Lancé si un document est chiffré avec un mot de passe et que le mot de passe spécifié lors de l'ouverture du document est incorrect ou manquant.

Pour en savoir plus, visitez le[Programmation avec des documents](https://docs.aspose.com/words/net/programming-with-documents/) article de documentation.

```csharp
public class IncorrectPasswordException : Exception
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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)

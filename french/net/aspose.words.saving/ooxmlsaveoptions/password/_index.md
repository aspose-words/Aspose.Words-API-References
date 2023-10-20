---
title: OoxmlSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words pour .NET
description: OoxmlSaveOptions Password propriété. Obtient/définit un mot de passe pour chiffrer le document à laide de lalgorithme de chiffrement standard ECMA376 en C#.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/ooxmlsaveoptions/password/
---
## OoxmlSaveOptions.Password property

Obtient/définit un mot de passe pour chiffrer le document à l'aide de l'algorithme de chiffrement standard ECMA376.

```csharp
public string Password { get; set; }
```

## Remarques

Afin d'enregistrer le document sans cryptage, cette propriété doit être`nul` ou une chaîne vide.

## Exemples

Montre comment créer un document Office Open XML chiffré par mot de passe.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Password.docx", saveOptions);

// Nous ne pourrons pas ouvrir ce document avec Microsoft Word ou
// Aspose.Words sans fournir le mot de passe correct.
Assert.Throws<IncorrectPasswordException>(() =>
    doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx"));

// Ouvrez le document chiffré en passant le mot de passe correct dans un objet LoadOptions.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx", new LoadOptions("MyPassword"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Voir également

* class [OoxmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)

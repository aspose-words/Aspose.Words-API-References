---
title: Font.NameAscii
linktitle: NameAscii
articleTitle: NameAscii
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Font NameAscii pour personnaliser les polices de texte latines, en améliorant votre conception avec des codes de caractères 0 à 127 pour une meilleure lisibilité.
type: docs
weight: 240
url: /fr/net/aspose.words/font/nameascii/
---
## Font.NameAscii property

Renvoie ou définit la police utilisée pour le texte latin (caractères avec des codes de caractère de 0 (zéro) à 127).

```csharp
public string NameAscii { get; set; }
```

## Exemples

Montre comment Microsoft Word peut combiner deux polices différentes en une seule exécution.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Supposons une exécution que nous utilisons le générateur pour insérer tout en utilisant cette configuration de police
// contient des caractères compris dans la plage de caractères ASCII. Dans ce cas,
// il affichera ces caractères en utilisant cette police.
builder.Font.NameAscii = "Calibri";

// Sans autre police spécifiée, le générateur appliquera également cette police à tous les caractères qu'il insère.
Assert.AreEqual("Calibri", builder.Font.Name);

// Spécifiez une police à utiliser pour tous les caractères en dehors de la plage ASCII.
// Idéalement, cette police devrait avoir un glyphe pour chaque code de caractère non ASCII requis.
builder.Font.NameOther = "Courier New";

// Insérer une séquence avec un mot composé de caractères ASCII et un mot avec tous les caractères en dehors de cette plage.
// Chaque caractère sera affiché en utilisant l'une ou l'autre des polices, selon.
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### Voir également

* property [Name](../name/)
* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

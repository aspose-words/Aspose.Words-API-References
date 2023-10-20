---
title: Font.NameOther
linktitle: NameOther
articleTitle: NameOther
second_title: Aspose.Words pour .NET
description: Font NameOther propriété. Renvoie ou définit la police utilisée pour les caractères avec des codes de caractères compris entre 128 et 255 en C#.
type: docs
weight: 270
url: /fr/net/aspose.words/font/nameother/
---
## Font.NameOther property

Renvoie ou définit la police utilisée pour les caractères avec des codes de caractères compris entre 128 et 255.

```csharp
public string NameOther { get; set; }
```

## Exemples

Montre comment Microsoft Word peut combiner deux polices différentes en une seule fois.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Supposons une exécution que nous utilisons le constructeur pour insérer en utilisant cette configuration de police
// contient des caractères dans la plage des caractères ASCII. Dans ce cas,
// il affichera ces caractères en utilisant cette police.
builder.Font.NameAscii = "Calibri";

// Sans autre police spécifiée, le constructeur appliquera également cette police à tous les caractères qu'il insère.
Assert.AreEqual("Calibri", builder.Font.Name);

// Spécifie une police à utiliser pour tous les caractères en dehors de la plage ASCII.
// Idéalement, cette police devrait avoir un glyphe pour chaque code de caractère non-ASCII requis.
builder.Font.NameOther = "Courier New";

// Insère une séquence avec un mot composé de caractères ASCII et un mot avec tous les caractères en dehors de cette plage.
// Chaque caractère sera affiché en utilisant l'une ou l'autre des polices, selon.
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### Voir également

* property [Name](../name/)
* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

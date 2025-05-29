---
title: Font.LocaleIdBi
linktitle: LocaleIdBi
articleTitle: LocaleIdBi
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Font LocaleIdBi, gérez facilement les identifiants régionaux pour les caractères formatés de droite à gauche, améliorant ainsi vos applications multilingues.
type: docs
weight: 210
url: /fr/net/aspose.words/font/localeidbi/
---
## Font.LocaleIdBi property

Obtient ou définit l'identifiant régional (langue) des caractères formatés de droite à gauche.

```csharp
public int LocaleIdBi { get; set; }
```

## Remarques

Pour la liste des identifiants de paramètres régionaux, voir https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Exemples

Montre comment définir des ensembles distincts de paramètres de police pour le texte de droite à gauche et de droite à gauche.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Définissez un ensemble de paramètres de police pour le texte de gauche à droite.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Définissez un autre ensemble de paramètres de police pour le texte de droite à gauche.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// Nous pouvons utiliser l'indicateur Bidi pour indiquer si le texte que nous sommes sur le point d'ajouter
// avec le générateur de documents, l'écriture s'effectue de droite à gauche. Lorsque nous ajoutons du texte avec cet indicateur à « vrai »,
// il sera formaté en utilisant l'ensemble de paramètres de police de droite à gauche.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Définissez l'indicateur sur faux, puis ajoutez du texte de gauche à droite.
// Le générateur de documents les formatera en utilisant l'ensemble de paramètres de police de gauche à droite.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

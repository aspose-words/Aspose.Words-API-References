---
title: Font.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Font Bidi, contrôlez les caractéristiques du texte de droite à gauche pour une lisibilité et une expérience utilisateur améliorées dans vos conceptions Web.
type: docs
weight: 30
url: /fr/net/aspose.words/font/bidi/
---
## Font.Bidi property

Spécifie si le contenu de cette exécution doit avoir des caractéristiques de droite à gauche.

```csharp
public bool Bidi { get; set; }
```

## Remarques

Cette propriété, lorsqu'elle est activée, ne doit pas être utilisée avec du texte fortement orienté de gauche à droite. Tout comportement sous cette condition n'est pas spécifié. Cette propriété, lorsqu'elle est désactivée, ne doit pas être utilisée avec du texte fortement orienté de droite à gauche. Tout comportement sous cette condition n'est pas spécifié.

Lors de l'affichage du contenu de cette séquence, tous les caractères seront traités comme des caractères de script complexes pour le formatage de x000d. Cela signifie que[`BoldBi`](../boldbi/) ,[`ItalicBi`](../italicbi/) ,[`SizeBi`](../sizebi/) et un nom de police correspondant sera utilisé lors du rendu de cette exécution.

De plus, lorsque le contenu de cette exécution est affiché, cette propriété agit comme un remplacement de droite à gauche pour les caractères qui sont classés comme « types faibles » et « types neutres ».

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

---
title: Font.SizeBi
linktitle: SizeBi
articleTitle: SizeBi
second_title: Aspose.Words pour .NET
description: Font SizeBi propriété. Obtient ou définit la taille de la police en points utilisée dans un document de droite à gauche en C#.
type: docs
weight: 350
url: /fr/net/aspose.words/font/sizebi/
---
## Font.SizeBi property

Obtient ou définit la taille de la police en points utilisée dans un document de droite à gauche.

```csharp
public double SizeBi { get; set; }
```

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

// Nous pouvons utiliser le drapeau Bidi pour indiquer si le texte que nous sommes sur le point d'ajouter
// avec le générateur de documents, c'est de droite à gauche. Lorsque nous ajoutons du texte avec cet indicateur défini sur true,
// il sera formaté en utilisant l'ensemble de paramètres de police de droite à gauche.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Définissez l'indicateur sur false, puis ajoutez du texte de gauche à droite.
// Le générateur de documents les formatera en utilisant l'ensemble de paramètres de police de gauche à droite.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

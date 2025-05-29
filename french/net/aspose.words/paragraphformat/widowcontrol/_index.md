---
title: ParagraphFormat.WidowControl
linktitle: WidowControl
articleTitle: WidowControl
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété ParagraphFormat WidowControl garantit que les première et dernière lignes de votre texte restent ensemble sur la même page pour une meilleure lisibilité.
type: docs
weight: 410
url: /fr/net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

Vrai si la première et la dernière ligne du paragraphe doivent rester sur la même page que le reste du paragraphe.

```csharp
public bool WidowControl { get; set; }
```

## Exemples

Montre comment activer le contrôle des veuves/orphelins pour un paragraphe.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lorsque nous écrivons un texte qui ne tient pas sur une page, une ligne peut déborder sur la page suivante.
// La seule ligne qui se termine sur la page suivante est appelée « Orphelin »,
// et la ligne précédente où l'orphelin s'est arrêté s'appelle une « Veuve ».
// Nous pouvons réparer les orphelins et les veuves en réorganisant le texte via la taille de la police, l'espacement ou les marges de page.
// Si nous souhaitons conserver les dimensions de notre document, nous pouvons définir cet indicateur sur « true »
// pour mettre les veuves sur la même page que leurs orphelins respectifs.
// Laissez cet indicateur sur « false » pour laisser les paires veuve/orpheline dans le texte.
// Chaque paragraphe a ce paramètre accessible dans Microsoft Word via Accueil -> Paragraphe -> Paramètres de paragraphe
// (bouton en bas à droite de l'onglet "Paragraphe") -> "Contrôle des veuves/orphelins".
builder.ParagraphFormat.WidowControl = widowControl; 

// Insérer du texte qui produit un orphelin et une veuve.
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### Voir également

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

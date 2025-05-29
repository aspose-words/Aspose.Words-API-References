---
title: DropCapPosition Enum
linktitle: DropCapPosition
articleTitle: DropCapPosition
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.DropCapPosition pour améliorer la conception de votre document en définissant des positions de texte en lettrine uniques pour un attrait visuel percutant.
type: docs
weight: 1820
url: /fr/net/aspose.words/dropcapposition/
---
## DropCapPosition enumeration

Spécifie la position d'un texte en lettrine.

```csharp
public enum DropCapPosition
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Le paragraphe n'a pas de lettrine. |
| Normal | `1` | La lettrine est positionnée à l'intérieur de la marge de texte sur le paragraphe d'ancrage. |
| Margin | `2` | La lettrine est positionnée à l'extérieur de la marge de texte sur le paragraphe d'ancrage. |

## Exemples

Montre comment créer une lettrine.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez un paragraphe avec une grande lettre par laquelle commence le texte des deuxième et troisième paragraphes.
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Actuellement, les deuxième et troisième paragraphes apparaîtront sous le premier.
// Nous pouvons convertir le premier paragraphe en lettrine pour les autres paragraphes via son objet "ParagraphFormat".
// Définissez la propriété « DropCapPosition » sur « DropCapPosition.Margin » pour placer la lettrine
// en dehors de la marge de gauche de la page si notre texte est de gauche à droite.
// Définissez la propriété « DropCapPosition » sur « DropCapPosition.Normal » pour placer la lettrine dans les marges de la page
// et d'envelopper le reste du texte autour.
// "DropCapPosition.None" est l'état par défaut pour tous les paragraphes.
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)

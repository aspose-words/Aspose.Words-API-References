---
title: DropCapPosition Enum
linktitle: DropCapPosition
articleTitle: DropCapPosition
second_title: Aspose.Words pour .NET
description: Aspose.Words.DropCapPosition énumération. Spécifie la position dun texte en lettrine en C#.
type: docs
weight: 1410
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
| Normal | `1` | La lettrine est positionnée à l'intérieur de la marge de texte du paragraphe d'ancrage. |
| Margin | `2` | La lettrine est positionnée en dehors de la marge de texte sur le paragraphe d'ancrage. |

## Exemples

Montre comment créer une lettrine.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère un paragraphe avec une grande lettre par laquelle commence le texte des deuxième et troisième paragraphes.
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Actuellement, les deuxième et troisième paragraphes apparaîtront sous le premier.
// On peut convertir le premier paragraphe en lettrine pour les autres paragraphes via son objet "ParagraphFormat".
// Définissez la propriété "DropCapPosition" sur "DropCapPosition.Margin" pour placer la lettrine
// en dehors de la marge gauche de la page si notre texte est de gauche à droite.
// Définissez la propriété "DropCapPosition" sur "DropCapPosition.Normal" pour placer la lettrine dans les marges de la page
// et pour envelopper le reste du texte autour.
// "DropCapPosition.None" est l'état par défaut pour tous les paragraphes.
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)

---
title: Font.Emboss
linktitle: Emboss
articleTitle: Emboss
second_title: Aspose.Words pour .NET
description: Découvrez la fonction Font Emboss, qui sublime votre texte avec un effet gaufré élégant pour des designs accrocheurs. Sublimez votre typographie dès aujourd'hui !
type: docs
weight: 100
url: /fr/net/aspose.words/font/emboss/
---
## Font.Emboss property

Vrai si la police est formatée en relief.

```csharp
public bool Emboss { get; set; }
```

## Exemples

Montre comment appliquer des effets de gravure/gaufrage au texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Color = Color.LightBlue;

// Vous trouverez ci-dessous deux manières d’utiliser les ombres pour appliquer un effet 3D au texte.
// 1 - Graver le texte pour donner l'impression que les lettres sont enfoncées dans la page :
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 - Mettez du texte en relief pour donner l'impression que les lettres sortent de la page :
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

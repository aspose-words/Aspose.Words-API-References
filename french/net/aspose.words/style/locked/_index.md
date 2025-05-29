---
title: Style.Locked
linktitle: Locked
articleTitle: Locked
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Style Locked, contrôlez le verrouillage des styles pour une flexibilité et une cohérence accrues dans vos projets. Libérez votre créativité dès aujourd'hui !
type: docs
weight: 120
url: /fr/net/aspose.words/style/locked/
---
## Style.Locked property

Spécifie si ce style est verrouillé.

```csharp
public bool Locked { get; set; }
```

## Exemples

Montre comment verrouiller le style.

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];
if (!styleHeading1.Locked)
    styleHeading1.Locked = true;

doc.Save(ArtifactsDir + "Styles.LockStyle.docx");
```

### Voir également

* class [Style](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

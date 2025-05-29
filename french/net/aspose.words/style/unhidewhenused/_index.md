---
title: Style.UnhideWhenUsed
linktitle: UnhideWhenUsed
articleTitle: UnhideWhenUsed
second_title: Aspose.Words pour .NET
description: Découvrez comment gérer la propriété UnhideWhenUsed pour les styles. Contrôlez la visibilité dans la galerie Styles et le volet Office pour améliorer la conception de votre document.
type: docs
weight: 210
url: /fr/net/aspose.words/style/unhidewhenused/
---
## Style.UnhideWhenUsed property

Obtient/définit si le style utilisé dans le document actuel est affiché dans la galerie Styles et dans le volet Office Styles. Vrai lorsque le style utilisé doit être affiché dans la galerie Styles.

```csharp
public bool UnhideWhenUsed { get; set; }
```

## Exemples

Montre comment prioriser et masquer un style.

```csharp
Document doc = new Document();
Style styleTitle = doc.Styles[StyleIdentifier.Subtitle];

if (styleTitle.Priority == 9)
    styleTitle.Priority = 10;

if (!styleTitle.UnhideWhenUsed)
    styleTitle.UnhideWhenUsed = true;

if (styleTitle.SemiHidden)
    styleTitle.SemiHidden = true;

doc.Save(ArtifactsDir + "Styles.StylePriority.docx");
```

### Voir également

* class [Style](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---
title: Style.SemiHidden
linktitle: SemiHidden
articleTitle: SemiHidden
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété SemiHidden contrôle la visibilité du style dans la galerie Styles et le volet des tâches, améliorant ainsi votre flux de travail de conception et votre efficacité.
type: docs
weight: 170
url: /fr/net/aspose.words/style/semihidden/
---
## Style.SemiHidden property

Obtient/définit si le style est masqué dans la galerie Styles et dans le volet Office Styles.

```csharp
public bool SemiHidden { get; set; }
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

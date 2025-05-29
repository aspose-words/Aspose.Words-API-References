---
title: Style.Priority
linktitle: Priority
articleTitle: Priority
second_title: Aspose.Words pour .NET
description: Découvrez comment gérer les paramètres de priorité des styles pour optimiser le tri des styles dans votre volet des tâches. Améliorez votre flux de travail grâce à une organisation efficace des styles !
type: docs
weight: 160
url: /fr/net/aspose.words/style/priority/
---
## Style.Priority property

Obtient/définit la valeur entière qui représente la priorité de tri des styles dans le volet Office Styles.

```csharp
public int Priority { get; set; }
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

---
title: WarningInfo.Source
linktitle: Source
articleTitle: Source
second_title: Aspose.Words pour .NET
description: Découvrez la propriété WarningInfo Source qui révèle l'origine des avertissements, améliorant ainsi la fiabilité de votre application et l'expérience utilisateur.
type: docs
weight: 20
url: /fr/net/aspose.words/warninginfo/source/
---
## WarningInfo.Source property

Renvoie la source de l'avertissement.

```csharp
public WarningSource Source { get; }
```

## Exemples

Montre comment travailler avec la source d'avertissement.

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.AreEqual("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.Description);
}
```

### Voir également

* enum [WarningSource](../../warningsource/)
* class [WarningInfo](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

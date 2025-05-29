---
title: NumSpacing Enum
linktitle: NumSpacing
articleTitle: NumSpacing
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.NumSpacing pour personnaliser l'espacement des chiffres et améliorer la mise en forme de vos documents. Améliorez vos présentations dès aujourd'hui !
type: docs
weight: 5030
url: /fr/net/aspose.words/numspacing/
---
## NumSpacing enumeration

Spécifie les valeurs possibles dans lesquelles l'espacement des chiffres peut être affiché.

```csharp
public enum NumSpacing
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Default | `0` | Spécifie que les chiffres sont affichés dans la forme par défaut de la police. |
| Proportional | `1` | Spécifie que les formes des chiffres conçues comme espacées proportionnellement sont affichées si elles sont prises en charge par la police. |
| Tabular | `2` | Spécifie que les formes des chiffres conçues comme tabulaires sont affichées si elles sont prises en charge par la police. |

## Exemples

Montre comment définir le type d'espacement du chiffre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cet effet n'est pris en charge que dans les versions plus récentes de MS Word.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2019);

builder.Write("1 ");
builder.Write("This is an example");

Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
if (run.Font.NumberSpacing == NumSpacing.Default)
    run.Font.NumberSpacing = NumSpacing.Proportional;

doc.Save(ArtifactsDir + "Fonts.NumberSpacing.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)

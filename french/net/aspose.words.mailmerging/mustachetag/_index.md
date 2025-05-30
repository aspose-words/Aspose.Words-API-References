---
title: MustacheTag Class
linktitle: MustacheTag
articleTitle: MustacheTag
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.MailMerging.MustacheTag  gérez efficacement les balises moustache pour une automatisation transparente des documents et une fusion de courrier améliorée.
type: docs
weight: 4570
url: /fr/net/aspose.words.mailmerging/mustachetag/
---
## MustacheTag class

Représente la balise « moustache ».

```csharp
public class MustacheTag
```

## Propriétés

| Nom | La description |
| --- | --- |
| [ReferenceOffset](../../aspose.words.mailmerging/mustachetag/referenceoffset/) { get; } | Obtient la position de départ de base zéro de la balise à partir du début de la[`ReferenceRun`](./referencerun/) . |
| [ReferenceRun](../../aspose.words.mailmerging/mustachetag/referencerun/) { get; } | Obtient l'exécution qui contient le début de la balise. |
| [Text](../../aspose.words.mailmerging/mustachetag/text/) { get; } | Obtient le texte de la balise. |

## Exemples

Montre comment travailler avec les balises de moustache.

```csharp
Document document = new Document(MyDir + "Mail merge mustache tags.docx");
document.MailMerge.UseNonMergeFields = true;

MailMergeRegionInfo hierarchy = document.MailMerge.GetRegionsHierarchy();

foreach (MustacheTag mustacheTag in hierarchy.MustacheTags)
{
    Console.WriteLine(mustacheTag.Text);
    Console.WriteLine(mustacheTag.ReferenceOffset);
    Console.WriteLine(mustacheTag.ReferenceRun);
}

foreach (MailMergeRegionInfo region in hierarchy.Regions)
{
    Console.WriteLine(region.StartMustacheTag.Text);
    Console.WriteLine(region.EndMustacheTag.Text);
}
```

### Voir également

* espace de noms [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../)

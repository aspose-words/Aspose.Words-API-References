---
title: MustacheTag.ReferenceOffset
linktitle: ReferenceOffset
articleTitle: ReferenceOffset
second_title: Aspose.Words pour .NET
description: Découvrez la propriété MustacheTag ReferenceOffset, qui révèle la position de départ basée sur zéro des balises dans votre ReferenceRun pour une gestion précise des données.
type: docs
weight: 10
url: /fr/net/aspose.words.mailmerging/mustachetag/referenceoffset/
---
## MustacheTag.ReferenceOffset property

Obtient la position de départ de base zéro de la balise à partir du début de la[`ReferenceRun`](../referencerun/) .

```csharp
public int ReferenceOffset { get; }
```

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

* class [MustacheTag](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)

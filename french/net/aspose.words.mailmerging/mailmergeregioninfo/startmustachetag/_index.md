---
title: MailMergeRegionInfo.StartMustacheTag
linktitle: StartMustacheTag
articleTitle: StartMustacheTag
second_title: Aspose.Words pour .NET
description: Découvrez la propriété MailMergeRegionInfo StartMustacheTag, qui fournit une balise de démarrage essentielle pour des régions de document transparentes dans vos projets.
type: docs
weight: 100
url: /fr/net/aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/
---
## MailMergeRegionInfo.StartMustacheTag property

Renvoie une balise de début « moustache » pour la région.

```csharp
public MustacheTag StartMustacheTag { get; }
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

* class [MustacheTag](../../mustachetag/)
* class [MailMergeRegionInfo](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)

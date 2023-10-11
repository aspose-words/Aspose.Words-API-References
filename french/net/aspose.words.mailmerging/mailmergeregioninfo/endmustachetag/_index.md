---
title: MailMergeRegionInfo.EndMustacheTag
second_title: Référence de l'API Aspose.Words pour .NET
description: MailMergeRegionInfo propriété. Renvoie une balise de fin moustache pour la région.
type: docs
weight: 20
url: /fr/net/aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/
---
## MailMergeRegionInfo.EndMustacheTag property

Renvoie une balise de fin "moustache" pour la région.

```csharp
public MustacheTag EndMustacheTag { get; }
```

### Exemples

Montre comment utiliser les balises de moustache.

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
* espace de noms [Aspose.Words.MailMerging](../../mailmergeregioninfo/)
* Assemblée [Aspose.Words](../../../)



---
title: MustacheTag.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words pour .NET
description: Découvrez la propriété MustacheTag Text pour récupérer et utiliser sans effort le texte des balises pour une gestion améliorée des données et une intégration transparente.
type: docs
weight: 30
url: /fr/net/aspose.words.mailmerging/mustachetag/text/
---
## MustacheTag.Text property

Obtient le texte de la balise.

```csharp
public string Text { get; }
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

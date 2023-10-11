---
title: MustacheTag.ReferenceRun
second_title: Référence de l'API Aspose.Words pour .NET
description: MustacheTag propriété. Obtient lexécution qui contient le début de la balise.
type: docs
weight: 20
url: /fr/net/aspose.words.mailmerging/mustachetag/referencerun/
---
## MustacheTag.ReferenceRun property

Obtient l'exécution qui contient le début de la balise.

```csharp
public Run ReferenceRun { get; }
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

* class [Run](../../../aspose.words/run/)
* class [MustacheTag](../)
* espace de noms [Aspose.Words.MailMerging](../../mustachetag/)
* Assemblée [Aspose.Words](../../../)



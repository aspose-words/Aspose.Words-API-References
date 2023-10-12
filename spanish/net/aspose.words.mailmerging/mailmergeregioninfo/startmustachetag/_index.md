---
title: MailMergeRegionInfo.StartMustacheTag
second_title: Referencia de API de Aspose.Words para .NET
description: MailMergeRegionInfo propiedad. Devuelve una etiqueta inicial bigote para la región.
type: docs
weight: 100
url: /es/net/aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/
---
## MailMergeRegionInfo.StartMustacheTag property

Devuelve una etiqueta inicial "bigote" para la región.

```csharp
public MustacheTag StartMustacheTag { get; }
```

### Ejemplos

Muestra cómo trabajar con las etiquetas de bigote.

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

### Ver también

* class [MustacheTag](../../mustachetag/)
* class [MailMergeRegionInfo](../)
* espacio de nombres [Aspose.Words.MailMerging](../../mailmergeregioninfo/)
* asamblea [Aspose.Words](../../../)



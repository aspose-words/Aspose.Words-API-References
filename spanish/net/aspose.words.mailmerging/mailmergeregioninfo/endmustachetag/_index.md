---
title: MailMergeRegionInfo.EndMustacheTag
linktitle: EndMustacheTag
articleTitle: EndMustacheTag
second_title: Aspose.Words para .NET
description: Descubra la propiedad MailMergeRegionInfo EndMustacheTag, que devuelve eficientemente la etiqueta de cierre de bigote para las regiones de su documento. ¡Optimice su flujo de trabajo!
type: docs
weight: 20
url: /es/net/aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/
---
## MailMergeRegionInfo.EndMustacheTag property

Devuelve una etiqueta "bigote" final para la región.

```csharp
public MustacheTag EndMustacheTag { get; }
```

## Ejemplos

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
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)

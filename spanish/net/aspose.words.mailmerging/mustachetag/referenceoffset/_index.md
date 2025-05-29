---
title: MustacheTag.ReferenceOffset
linktitle: ReferenceOffset
articleTitle: ReferenceOffset
second_title: Aspose.Words para .NET
description: Descubra la propiedad MustacheTag ReferenceOffset, que revela la posición inicial basada en cero de las etiquetas en su ReferenceRun para una gestión precisa de datos.
type: docs
weight: 10
url: /es/net/aspose.words.mailmerging/mustachetag/referenceoffset/
---
## MustacheTag.ReferenceOffset property

Obtiene la posición inicial basada en cero de la etiqueta desde el inicio de la[`ReferenceRun`](../referencerun/) .

```csharp
public int ReferenceOffset { get; }
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

* class [MustacheTag](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)

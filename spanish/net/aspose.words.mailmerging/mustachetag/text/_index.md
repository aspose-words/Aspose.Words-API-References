---
title: MustacheTag.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words para .NET
description: Descubra la propiedad Texto MustacheTag para recuperar y utilizar sin esfuerzo el texto de las etiquetas para un mejor manejo de datos y una integración perfecta.
type: docs
weight: 30
url: /es/net/aspose.words.mailmerging/mustachetag/text/
---
## MustacheTag.Text property

Obtiene el texto de la etiqueta.

```csharp
public string Text { get; }
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

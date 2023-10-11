---
title: MustacheTag.Text
second_title: Aspose.Words per .NET API Reference
description: MustacheTag proprietà. Ottiene il testo del tag.
type: docs
weight: 30
url: /it/net/aspose.words.mailmerging/mustachetag/text/
---
## MustacheTag.Text property

Ottiene il testo del tag.

```csharp
public string Text { get; }
```

### Esempi

Mostra come lavorare con le etichette dei baffi.

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

### Guarda anche

* class [MustacheTag](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../mustachetag/)
* assemblea [Aspose.Words](../../../)



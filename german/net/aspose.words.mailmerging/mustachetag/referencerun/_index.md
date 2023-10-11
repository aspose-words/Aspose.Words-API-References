---
title: MustacheTag.ReferenceRun
second_title: Aspose.Words für .NET-API-Referenz
description: MustacheTag eigendom. Ruft den Lauf ab der den Anfang des Tags enthält.
type: docs
weight: 20
url: /de/net/aspose.words.mailmerging/mustachetag/referencerun/
---
## MustacheTag.ReferenceRun property

Ruft den Lauf ab, der den Anfang des Tags enthält.

```csharp
public Run ReferenceRun { get; }
```

### Beispiele

Zeigt, wie mit den Moustache-Tags gearbeitet wird.

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

### Siehe auch

* class [Run](../../../aspose.words/run/)
* class [MustacheTag](../)
* namensraum [Aspose.Words.MailMerging](../../mustachetag/)
* Montage [Aspose.Words](../../../)



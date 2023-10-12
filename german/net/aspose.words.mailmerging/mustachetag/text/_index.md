---
title: MustacheTag.Text
second_title: Aspose.Words für .NET-API-Referenz
description: MustacheTag eigendom. Ruft den Text des Tags ab.
type: docs
weight: 30
url: /de/net/aspose.words.mailmerging/mustachetag/text/
---
## MustacheTag.Text property

Ruft den Text des Tags ab.

```csharp
public string Text { get; }
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

* class [MustacheTag](../)
* namensraum [Aspose.Words.MailMerging](../../mustachetag/)
* Montage [Aspose.Words](../../../)



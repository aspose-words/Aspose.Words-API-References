---
title: MarkdownSaveOptions.ListExportMode
linktitle: ListExportMode
articleTitle: ListExportMode
second_title: .NET için Aspose.Words
description: MarkdownSaveOptions'ın liste öğelerinin nasıl çıktı alınacağını kontrol eden ListExportMode özelliğini keşfedin. Esnek MarkdownSyntax ile dosyalarınızı optimize edin!
type: docs
weight: 110
url: /tr/net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

Liste öğelerinin çıktı dosyasına nasıl yazılacağını belirtir. Varsayılan değerMarkdownSyntax .

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

## Notlar

Bu özellik şu şekilde ayarlandığında:PlainText tüm liste etiketleri are kullanılarak güncellendi[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) ve gerçek değerleriyle dışa aktarılır. Bu tür lists Markdown biçimiyle uyumlu olmayabilir ve bu durumda içe aktarıldığında düz metin olarak tanınacaktır.

Bu özellik şu şekilde ayarlandığında:MarkdownSyntaxYazar, liste öğelerini Markdown tarafından otomatik modda numaralandırmaya izin verecek şekilde export liste öğelerini denemeye çalışır.

## Örnekler

Öğelerin listelenmesinin markdown belgesine nasıl yazılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Listeyi dışa aktarmak için MarkdownListExportMode.PlainText veya MarkdownListExportMode.MarkdownSyntax'ı kullanın.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### Ayrıca bakınız

* enum [MarkdownListExportMode](../../markdownlistexportmode/)
* class [MarkdownSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)

---
title: MarkdownSaveOptions.ListExportMode
second_title: Aspose.Words for .NET API Referansı
description: MarkdownSaveOptions mülk. Liste öğelerinin çıktı dosyasına nasıl yazılacağını belirtir. Varsayılan değerMarkdownSyntax .
type: docs
weight: 60
url: /tr/net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

Liste öğelerinin çıktı dosyasına nasıl yazılacağını belirtir. Varsayılan değer:MarkdownSyntax .

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

### Notlar

Bu özellik olarak ayarlandığındaPlainText tüm liste etiketleri are kullanılarak güncellendi[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/)gerçek değerleri ile ihraç edilmektedir. Bu tür listeler , Markdown formatıyla uyumlu olmayabilir ve bu durumda içe aktarma sırasında düz metin olarak tanınacaktır.

Bu özellik olarak ayarlandığındaMarkdownSyntax, yazar Markdown tarafından otomatik modda liste öğelerinin numaralandırılmasına izin verecek şekildeexport liste öğelerini aktarmaya çalışır.

### Örnekler

Markdown belgesine yazılacak öğelerin nasıl listeleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Listeyi dışa aktarmak için MarkdownListExportMode.PlainText veya MarkdownListExportMode.MarkdownSyntax'ı kullanın.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### Ayrıca bakınız

* enum [MarkdownListExportMode](../../markdownlistexportmode/)
* class [MarkdownSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../markdownsaveoptions/)
* toplantı [Aspose.Words](../../../)



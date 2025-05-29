---
title: MarkdownSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: .NET için Aspose.Words
description: Markdown dışa aktarımlarınızı ImageResolution özelliğiyle optimize edin ve daha keskin görüntüler için özel çıktı çözünürlükleri ayarlayın. Varsayılan, 96 dpi.
type: docs
weight: 60
url: /tr/net/aspose.words.saving/markdownsaveoptions/imageresolution/
---
## MarkdownSaveOptions.ImageResolution property

Markdown'a aktarırken görüntülerin çıktı çözünürlüğünü belirtir. Varsayılan`96 dpi` .

```csharp
public int ImageResolution { get; set; }
```

## Örnekler

Görüntülerin çıktı çözünürlüğünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ImageResolution = 300;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

### Ayrıca bakınız

* class [MarkdownSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)

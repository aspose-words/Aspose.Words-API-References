---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode yöntemi"
linktitle: "get_ListExportMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode yöntemi. Liste öğelerinin çıktı dosyasına nasıl yazılacağını belirtir. Varsayılan değer C++'ta MarkdownSyntax'tir."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.saving/markdownsaveoptions/get_listexportmode/
---
## MarkdownSaveOptions::get_ListExportMode method


Liste öğelerinin çıktı dosyasına nasıl yazılacağını belirtir. Varsayılan değer [MarkdownSyntax](../../markdownlistexportmode/).

```cpp
Aspose::Words::Saving::MarkdownListExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode() const
```

## Açıklamalar


Bu özellik [PlainText](../../markdownlistexportmode/) olarak ayarlandığında, tüm liste etiketleri [UpdateListLabels](../../../aspose.words/document/updatelistlabels/) kullanılarak güncellenir ve gerçek değerleriyle dışa aktarılır. Böyle listeler Markdown formatıyla uyumsuz olabilir ve bu durumda içe aktarma sırasında düz metin olarak tanınır.

Bu özellik [MarkdownSyntax](../../markdownlistexportmode/) olarak ayarlandığında, yazar liste öğelerini Markdown ile otomatik numaralandırma moduna izin verecek şekilde dışa aktarmaya çalışır.

## Örnekler



Liste öğelerinin markdown belgesine nasıl yazılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// Listeyi dışa aktarmak için MarkdownListExportMode.PlainText veya MarkdownListExportMode.MarkdownSyntax kullanın.
auto options = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
options->set_ListExportMode(markdownListExportMode);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ListExportMode.md", options);
```

## Ayrıca Bakınız

* Enum [MarkdownListExportMode](../../markdownlistexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

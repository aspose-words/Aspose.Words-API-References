---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting metodu"
linktitle: "get_ExportUnderlineFormatting"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting metodu. Altı çizili metin biçimlendirmesini iki artı karakteri \"++\" dizisi olarak dışa aktarılıp aktarılmayacağını belirten bir bool değeri alır veya ayarlar. Varsayılan değer C++'da false'tur."
type: docs
weight: 3500
url: /tr/cpp/aspose.words.saving/markdownsaveoptions/get_exportunderlineformatting/
---
## MarkdownSaveOptions::get_ExportUnderlineFormatting method


Altı çizili metin biçimlendirmesini iki artı işareti "++" dizisi olarak dışa aktarılıp aktarılmayacağını gösteren bir boolean değer alır veya ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting() const
```


## Örnekler



Altı çizili biçimlendirmesinin ++ olarak nasıl dışa aktarılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Single);
builder->Write(u"Lorem ipsum. Dolor sit amet.");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportUnderlineFormatting(true);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

## Ayrıca Bakınız

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

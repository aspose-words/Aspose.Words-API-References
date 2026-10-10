---
title: "Aspose::Words::Saving::FontSavingArgs::get_FontFileName yöntemi"
linktitle: "get_FontFileName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::FontSavingArgs::get_FontFileName yöntemi. C++'da yazı tipinin kaydedileceği dosya adını (yol olmadan) alır veya ayarlar."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.saving/fontsavingargs/get_fontfilename/
---
## FontSavingArgs::get_FontFileName method


Yazı tipinin kaydedileceği dosya adını (yol olmadan) alır veya ayarlar.

```cpp
System::String Aspose::Words::Saving::FontSavingArgs::get_FontFileName() const
```

## Açıklamalar


Bu özellik, HTML'ye dışa aktarım sırasında yazı tipi dosya adlarının nasıl oluşturulduğunu yeniden tanımlamanıza olanak tanır.

Olay tetiklendiğinde, bu özellik Aspose.Words tarafından oluşturulan dosya adını içerir. Bu özelliğin değerini değiştirerek yazı tipini farklı bir dosyaya kaydedebilirsiniz. Dosya adlarının benzersiz olması gerektiğini unutmayın.

Aspose.Words, HTML formatına dışa aktarırken gömülü her yazı tipi için otomatik olarak benzersiz bir dosya adı oluşturur. Yazı tipi dosya adının nasıl oluşturulacağı, belgenin bir dosyaya mı yoksa bir akışa mı kaydedildiğine bağlıdır.

Bir belge bir dosyaya kaydedildiğinde, oluşturulan yazı tipi dosya adı şu şekilde görünür: *%<document base file name>.<original file name><optional suffix>.<extension>*.

Bir belge bir akışa kaydedildiğinde, oluşturulan yazı tipi dosya adı şu şekilde görünür: *Aspose.Words.<document guid>.<original file name><optional suffix>.<extension>*.

[FontFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name, the [FontsFolder](../../htmlsaveoptions/get_fontsfolder/) and [FontsFolderAlias](../../htmlsaveoptions/get_fontsfolderalias/) properties.

## Ayrıca Bakınız

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

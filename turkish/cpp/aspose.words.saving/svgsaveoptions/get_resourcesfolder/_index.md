---
title: "Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder yöntemi"
linktitle: "get_ResourcesFolder"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder yöntemi. Bir belge Svg formatına dışa aktarılırken kaynakların (görüntülerin) kaydedildiği fiziksel klasörü belirtir. Varsayılan değer C++'ta null'dır."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.saving/svgsaveoptions/get_resourcesfolder/
---
## SvgSaveOptions::get_ResourcesFolder method


Bir belge Svg formatına dışa aktarılırken kaynakların (görüntülerin) kaydedildiği fiziksel klasörü belirtir. Varsayılan **null**'dur.

```cpp
System::String Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder() const
```

## Açıklamalar


Yalnızca [ExportEmbeddedImages](../get_exportembeddedimages/) özelliği **false** olduğunda etkili olur.

Bir [Document](../../../aspose.words/document/) belgesini SVG formatında kaydettiğinizde, Aspose.Words tüm gömülü görüntüleri bağımsız dosyalar olarak kaydetmek zorundadır. [ResourcesFolder](./) görüntülerin nereye kaydedileceğini belirtmenizi sağlar ve [ResourcesFolderAlias](../get_resourcesfolderalias/) görüntü URI'lerinin nasıl oluşturulacağını belirtmenize olanak tanır.

Bir belgeyi bir dosyaya kaydedip dosya adı sağlarsanız, Aspose.Words varsayılan olarak görüntüleri belgenin kaydedildiği aynı klasöre kaydeder. Bu davranışı geçersiz kılmak için [ResourcesFolder](./) kullanın.

Bir belgeyi bir akışa kaydederseniz, Aspose.Words görüntüleri kaydedecek bir klasöre sahip olmaz, ancak yine de görüntüleri bir yerde kaydetmesi gerekir. Bu durumda, [ResourcesFolder](./) özelliğinde erişilebilir bir klasör belirtmeniz gerekir.

## Ayrıca Bakınız

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

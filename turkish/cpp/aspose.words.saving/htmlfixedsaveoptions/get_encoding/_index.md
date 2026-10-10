---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding metodu"
linktitle: "get_Encoding"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding metodu. HTML'ye dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer C++'da new UTF8Encoding(true) (BOM'lu UTF-8)'dir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_encoding/
---
## HtmlFixedSaveOptions::get_Encoding method


HTML'ye dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer **new UTF8Encoding(true)** (BOM'lu UTF-8).

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding() const
```


## Örnekler



Bir belgeyi HTML'ye dışa aktarırken hangi kodlamanın kullanılacağını nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello World!");

// Varsayılan kodlama UTF-8'dir. Belgemizi farklı bir kodlama kullanarak temsil etmek istiyorsak,
// Belirli bir kodlamayı ayarlamak için bir SaveOptions nesnesi kullanabiliriz.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_Encoding(System::Text::Encoding::get_ASCII());

ASSERT_EQ(u"US-ASCII", htmlFixedSaveOptions->get_Encoding()->get_EncodingName());

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

## Ayrıca Bakınız

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

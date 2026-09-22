---
title: "Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape method"
linktitle: "get_DisplayBackgroundShape"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape method. Arka plan şeklinin baskı düzeni görünümünde C++'da görüntülenmesini kontrol eder."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.settings/viewoptions/get_displaybackgroundshape/
---
## ViewOptions::get_DisplayBackgroundShape method


Yazdırma düzeni görünümünde arka plan şeklinin görüntülenmesini kontrol eder.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape() const
```


## Örnekler



Görünüm seçeneklerinde belge arka plan görüntülerini gizleme/gösterme yöntemini gösterir.
```cpp
// Düz bir arka plan rengine sahip yeni bir belge oluşturmak için bir HTML dizesi kullanın.
const System::String html = u"<html>\r\n                <body style='background-color: blue'>\r\n                    <p>Hello world!</p>\r\n                </body>\r\n            </html>";

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_Unicode()->GetBytes(html)));

// Belgenin kaynağı düz renkli bir arka plana sahiptir,
// bu varlık "DisplayBackgroundShape" bayrağını "true" olarak ayarlayacaktır.
ASSERT_TRUE(doc->get_ViewOptions()->get_DisplayBackgroundShape());

// Belgenin arka plan rengini görüntülemesi için "DisplayBackgroundShape" değerini "true" tutun.
// Bu, görünürlüğü artırmak için bazı metin renklerini etkileyebilir.
// Arka plan rengini görüntülememek için "DisplayBackgroundShape" değerini "false" olarak ayarlayın.
doc->get_ViewOptions()->set_DisplayBackgroundShape(displayBackgroundShape);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayBackgroundShape.docx");
```

## Ayrıca Bakınız

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)

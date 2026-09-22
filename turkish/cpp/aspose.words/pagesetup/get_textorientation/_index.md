---
title: "Aspose::Words::PageSetup::get_TextOrientation yöntemi"
linktitle: "get_TextOrientation"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_TextOrientation yöntemi. Tüm sayfa için TextOrientation belirtmeye izin verir. Varsayılan değer C++'da Horizontal'dır."
type: docs
weight: 45000
url: /tr/cpp/aspose.words/pagesetup/get_textorientation/
---
## PageSetup::get_TextOrientation method


Tüm sayfa için [TextOrientation](./) belirtmeye izin verir. Varsayılan değer [Horizontal](../../textorientation/)'dır.

```cpp
Aspose::Words::TextOrientation Aspose::Words::PageSetup::get_TextOrientation()
```


## Örnekler



Metin yönlendirmesinin nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// "TextOrientation" özelliğini "TextOrientation.Upward" olarak ayarlayarak tüm metni 90 derece döndürün
// sağa doğru, böylece tüm soldan sağa metin artık üstten alta gider.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TextOrientation(Aspose::Words::TextOrientation::Upward);

doc->Save(get_ArtifactsDir() + u"PageSetup.SetTextOrientation.docx");
```

## Ayrıca Bakınız

* Enum [TextOrientation](../../textorientation/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

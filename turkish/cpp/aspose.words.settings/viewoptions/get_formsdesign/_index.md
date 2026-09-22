---
title: "Aspose::Words::Settings::ViewOptions::get_FormsDesign yöntemi"
linktitle: "get_FormsDesign"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::ViewOptions::get_FormsDesign yöntemi. C++'ta belgenin form tasarım modunda olup olmadığını belirtir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.settings/viewoptions/get_formsdesign/
---
## ViewOptions::get_FormsDesign method


Belgenin form tasarım modunda olup olmadığını belirtir.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_FormsDesign() const
```

## Açıklamalar


Şu anda yalnızca WordML formatındaki belgeler için çalışır.

## Örnekler



Form tasarım modunu nasıl etkinleştireceğinizi/devre dışı bırakacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// \"FormsDesign\" özelliğini \"false\" olarak ayarlayarak form tasarım modunu devre dışı bırakın.
// \"FormsDesign\" özelliğini \"true\" olarak ayarlayarak form tasarım modunu etkinleştirin.
doc->get_ViewOptions()->set_FormsDesign(useFormsDesign);

doc->Save(get_ArtifactsDir() + u"ViewOptions.FormsDesign.xml");

ASPOSE_ASSERT_EQ(useFormsDesign, System::IO::File::ReadAllText(get_ArtifactsDir() + u"ViewOptions.FormsDesign.xml").Contains(u"<w:formsDesign />"));
```

## Ayrıca Bakınız

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)

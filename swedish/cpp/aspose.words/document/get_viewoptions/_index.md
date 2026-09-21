---
title: "Aspose::Words::Document::get_ViewOptions metod"
linktitle: "get_ViewOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_ViewOptions metod. Tillhandahåller alternativ för att styra hur dokumentet visas i Microsoft Word i C++."
type: docs
weight: 58000
url: /sv/cpp/aspose.words/document/get_viewoptions/
---
## Document::get_ViewOptions method


Tillhandahåller alternativ för att styra hur dokumentet visas i Microsoft Word.

```cpp
System::SharedPtr<Aspose::Words::Settings::ViewOptions> Aspose::Words::Document::get_ViewOptions()
```


## Exempel



Visar hur man ställer in en anpassad zoomfaktor, som äldre versioner av Microsoft Word kommer att tillämpa på ett dokument vid inläsning.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->get_ViewOptions()->set_ViewType(Aspose::Words::Settings::ViewType::PageLayout);
doc->get_ViewOptions()->set_ZoomPercent(50);

ASSERT_EQ(Aspose::Words::Settings::ZoomType::Custom, doc->get_ViewOptions()->get_ZoomType());
ASSERT_EQ(Aspose::Words::Settings::ZoomType::None, doc->get_ViewOptions()->get_ZoomType());

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomPercentage.doc");
```


Visar hur man ställer in en anpassad zoomtyp, som äldre versioner av Microsoft Word kommer att tillämpa på ett dokument vid inläsning.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Ställ in egenskapen "ZoomType" till "ZoomType.PageWidth" för att få Microsoft Word
// för att automatiskt zooma dokumentet så att det passar sidans bredd.
// Ställ in egenskapen "ZoomType" till "ZoomType.FullPage" för att få Microsoft Word
// för att automatiskt zooma dokumentet så att hela första sidan blir synlig.
// Ställ in egenskapen "ZoomType" till "ZoomType.TextFit" för att få Microsoft Word
// för att automatiskt zooma dokumentet så att det passar de inre textmarginalerna på första sidan.
doc->get_ViewOptions()->set_ZoomType(zoomType);

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomType.doc");
```

## Se även

* Class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

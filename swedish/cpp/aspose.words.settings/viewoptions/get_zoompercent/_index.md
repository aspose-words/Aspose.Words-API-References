---
title: "Aspose::Words::Settings::ViewOptions::get_ZoomPercent metod"
linktitle: "get_ZoomPercent"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::ViewOptions::get_ZoomPercent metod. Hämtar eller anger den procentandel du vill visa ditt dokument i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.settings/viewoptions/get_zoompercent/
---
## ViewOptions::get_ZoomPercent method


Hämtar eller anger den procentandel du vill visa ditt dokument i.

```cpp
int32_t Aspose::Words::Settings::ViewOptions::get_ZoomPercent() const
```

## Anmärkningar


Även om Aspose.Words kan läsa och skriva detta alternativ, är dess användning applikationsspecifik. Till exempel respekterar inte MS Word 2013 värdet på detta alternativ.

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

## Se även

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)

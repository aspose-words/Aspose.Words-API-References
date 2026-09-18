---
title: "Aspose::Words::Document::get_ViewOptions Methode"
linktitle: "get_ViewOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_ViewOptions Methode. Bietet Optionen zur Steuerung, wie das Dokument in Microsoft Word in C++ angezeigt wird."
type: docs
weight: 58000
url: /de/cpp/aspose.words/document/get_viewoptions/
---
## Document::get_ViewOptions method


Bietet Optionen, um zu steuern, wie das Dokument in Microsoft Word angezeigt wird.

```cpp
System::SharedPtr<Aspose::Words::Settings::ViewOptions> Aspose::Words::Document::get_ViewOptions()
```


## Beispiele



Zeigt, wie ein benutzerdefinierter Zoomfaktor festgelegt wird, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.
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


Zeigt, wie ein benutzerdefinierter Zoomtyp festgelegt wird, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Setzen Sie die Eigenschaft "ZoomType" auf "ZoomType.PageWidth", um Microsoft Word zu erhalten.
// um das Dokument automatisch zu zoomen, sodass es die Seitenbreite ausfüllt.
// Setzen Sie die Eigenschaft "ZoomType" auf "ZoomType.FullPage", um Microsoft Word zu erhalten.
// um das Dokument automatisch zu zoomen, sodass die gesamte erste Seite sichtbar wird.
// Setzen Sie die Eigenschaft "ZoomType" auf "ZoomType.TextFit", um Microsoft Word zu erhalten.
// um das Dokument automatisch zu zoomen, sodass die inneren Textränder der ersten Seite passen.
doc->get_ViewOptions()->set_ZoomType(zoomType);

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomType.doc");
```

## Siehe auch

* Class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

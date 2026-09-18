---
title: "Aspose::Words::Settings::ViewOptions::get_ZoomPercent Methode"
linktitle: "get_ZoomPercent"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::ViewOptions::get_ZoomPercent Methode. Liest oder setzt den Prozentsatz, mit dem Sie Ihr Dokument in C++ anzeigen möchten."
type: docs
weight: 6000
url: /de/cpp/aspose.words.settings/viewoptions/get_zoompercent/
---
## ViewOptions::get_ZoomPercent method


Liest oder legt den Prozentsatz fest, mit dem Sie Ihr Dokument anzeigen möchten.

```cpp
int32_t Aspose::Words::Settings::ViewOptions::get_ZoomPercent() const
```

## Hinweise


Obwohl Aspose.Words diese Option lesen und schreiben kann, ist ihre Verwendung anwendungsspezifisch. Zum Beispiel respektiert MS Word 2013 den Wert dieser Option nicht.

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

## Siehe auch

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)

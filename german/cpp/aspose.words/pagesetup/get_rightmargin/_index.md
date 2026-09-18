---
title: "Aspose::Words::PageSetup::get_RightMargin Methode"
linktitle: "get_RightMargin"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_RightMargin Methode. Gibt den Abstand (in Punkten) zwischen dem rechten Rand der Seite und der rechten Begrenzung des Fließtextes zurück oder setzt ihn in C++."
type: docs
weight: 39000
url: /de/cpp/aspose.words/pagesetup/get_rightmargin/
---
## PageSetup::get_RightMargin method


Gibt den Abstand (in Punkten) zwischen dem rechten Rand der Seite und der rechten Begrenzung des Fließtextes zurück oder legt ihn fest.

```cpp
double Aspose::Words::PageSetup::get_RightMargin()
```


## Beispiele



Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Legal);
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_HeaderDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));
builder->get_PageSetup()->set_FooterDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));

builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PageSetup.PageMargins.docx");
```

## Siehe auch

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Aspose::Words::PageSetup::get_PageHeight-Methode"
linktitle: "get_PageHeight"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_PageHeight-Methode. Gibt die Höhe der Seite in Punkten zurück oder legt sie fest in C++."
type: docs
weight: 33000
url: /de/cpp/aspose.words/pagesetup/get_pageheight/
---
## PageSetup::get_PageHeight method


Gibt die Höhe der Seite in Punkten zurück oder legt sie fest.

```cpp
double Aspose::Words::PageSetup::get_PageHeight()
```


## Beispiele



Zeigt, wie man ein Bild einfügt und es als Wasserzeichen verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie das Bild in die Kopfzeile ein, damit es auf jeder Seite sichtbar ist.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);

// Platzieren Sie das Bild in der Mitte der Seite.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertWatermark.docx");
```

## Siehe auch

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Aspose::Words::Drawing::WrapType enum"
linktitle: "WrapType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::WrapType enum. Gibt an, wie Text um eine Form oder ein Bild in C++ gewickelt wird."
type: docs
weight: 45000
url: /de/cpp/aspose.words.drawing/wraptype/
---
## WrapType enum


Gibt an, wie Text um eine Form oder ein Bild herum umbrochen wird.

```cpp
enum class WrapType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 3 | Kein Textumbruch um die Form. Die Form wird hinter oder vor dem Text platziert. |
| Inline | 0 | Die Form bleibt auf derselben Ebene wie der Text und wird als Zeichen behandelt. |
| TopBottom | 1 | Der Text stoppt oben an der Form und beginnt in der Zeile unterhalb der Form neu. |
| Square | 2 | Umwickelt den Text um alle Seiten des quadratischen Begrenzungsrahmens der Form. |
| Tight | 4 | Umwickelt die Kanten der Form eng, anstatt um den Begrenzungsrahmen zu wickeln. |
| Through | 5 | Wie Tight, aber wickelt innerhalb aller offenen Teile der Form. |


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


Zeigt, wie man ein schwebendes Bild in die Mitte einer Seite einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein schwebendes Bild ein, das hinter dem überlappenden Text erscheint und es an der Seitenmitte ausrichtet.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)

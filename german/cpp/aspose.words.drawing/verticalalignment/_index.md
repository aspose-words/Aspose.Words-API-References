---
title: "Aspose::Words::Drawing::VerticalAlignment enum"
linktitle: "VerticalAlignment"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::VerticalAlignment enum. Gibt die vertikale Ausrichtung einer schwebenden Form, eines Textfelds oder einer schwebenden Tabelle in C++ an."
type: docs
weight: 43000
url: /de/cpp/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enum


Gibt die vertikale Ausrichtung einer schwebenden Form, eines Textfelds oder einer schwebenden Tabelle an.

```cpp
enum class VerticalAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Das Objekt wird explizit positioniert, normalerweise über seine **Top**‑Eigenschaft. |
| Oben | 1 | Gibt an, dass das Objekt am oberen Rand der vertikalen Ausrichtungsbasis liegen soll. |
| Mitte | 2 | Gibt an, dass das Objekt relativ zur vertikalen Ausrichtungsbasis zentriert sein soll. |
| Unten | 3 | Gibt an, dass das Objekt am unteren Ende der vertikalen Ausrichtungsbasis sein soll. |
| Inside | 4 | Gibt an, dass das Objekt innerhalb der horizontalen Ausrichtungsbasis sein soll. |
| Außerhalb | 5 | Gibt an, dass das Objekt außerhalb der vertikalen Ausrichtungsbasis sein soll. |
| Inline | -1 | Nicht dokumentiert. Scheint ein möglicher Wert für schwebende Absätze und Tabellen zu sein. |
| Default | n/a | Entspricht [None](./). |


## Beispiele



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

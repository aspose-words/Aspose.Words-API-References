---
title: "Aspose::Words::Drawing::HorizontalAlignment enum"
linktitle: "HorizontalAlignment"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::HorizontalAlignment enum. Gibt die horizontale Ausrichtung eines schwebenden Shapes, Textfelds oder einer schwebenden Tabelle in C++ an."
type: docs
weight: 26000
url: /de/cpp/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enum


Gibt die horizontale Ausrichtung einer schwebenden Form, eines Textfelds oder einer schwebenden Tabelle an.

```cpp
enum class HorizontalAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Das Objekt wird explizit positioniert, normalerweise über seine **Left**-Eigenschaft. |
| Default | n/a | Entspricht [None](./). |
| Links | 1 | Gibt an, dass das Objekt linksbündig zur horizontalen Ausrichtungsbasis ausgerichtet werden soll. |
| Mitte | 2 | Gibt an, dass das Objekt relativ zur horizontalen Ausrichtungsbasis zentriert werden soll. |
| Rechts | 3 | Gibt an, dass das Objekt rechtsbündig zur horizontalen Ausrichtungsbasis ausgerichtet werden soll. |
| Inside | 4 | Gibt an, dass das Objekt innerhalb der horizontalen Ausrichtungsbasis sein soll. |
| Außerhalb | 5 | Gibt an, dass das Objekt außerhalb der horizontalen Ausrichtungsbasis liegen soll. |


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

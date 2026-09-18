---
title: "Aspose::Words::Drawing::RelativeVerticalPosition enum"
linktitle: "RelativeVerticalPosition"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::RelativeVerticalPosition enum. Gibt an, worauf sich die vertikale Position einer Form oder eines Textrahmens in C++ bezieht."
type: docs
weight: 34000
url: /de/cpp/aspose.words.drawing/relativeverticalposition/
---
## RelativeVerticalPosition enum


Gibt an, worauf sich die vertikale Position einer Form oder eines Textfelds bezieht.

```cpp
enum class RelativeVerticalPosition
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Rand | 0 | Gibt an, dass die vertikale Positionierung relativ zu den Seitenrändern sein soll. |
| Page | 1 | Das Objekt ist relativ zur oberen Kante der Seite positioniert. |
| Paragraph | 2 | Das Objekt ist relativ zum oberen Rand des Absatzes positioniert, der den Anker enthält. |
| Linie | 3 | Undokumentiert. |
| TopMargin | 4 | Gibt an, dass die vertikale Positionierung relativ zum oberen Rand der aktuellen Seite sein soll. |
| BottomMargin | 5 | Gibt an, dass die vertikale Positionierung relativ zum unteren Rand der aktuellen Seite sein soll. |
| InsideMargin | 6 | Gibt an, dass die vertikale Positionierung relativ zum inneren Rand der aktuellen Seite sein soll. |
| OutsideMargin | 7 | Gibt an, dass die vertikale Positionierung relativ zum äußeren Rand der aktuellen Seite sein soll. |
| TableDefault | n/a | Standardwert ist [Margin](./). |
| TextFrameDefault | n/a | Standardwert ist [Paragraph](./). |


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

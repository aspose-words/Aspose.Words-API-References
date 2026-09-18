---
title: "Aspose::Words::Drawing::RelativeHorizontalPosition enum"
linktitle: "RelativeHorizontalPosition"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::RelativeHorizontalPosition enum. Gibt an, zu welchem Bezug die horizontale Position einer Form oder eines Textfelds in C++ relativ ist."
type: docs
weight: 33000
url: /de/cpp/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enum


Gibt an, worauf sich die horizontale Position einer Form oder eines Textfelds bezieht.

```cpp
enum class RelativeHorizontalPosition
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Rand | 0 | Gibt an, dass die horizontale Positionierung relativ zu den Seitenrändern sein soll. |
| Page | 1 | Das Objekt ist relativ zur linken Kante der Seite positioniert. |
| Spalte | 2 | Das Objekt ist relativ zur linken Seite der Spalte positioniert. |
| Character | 3 | Das Objekt ist relativ zur linken Seite des Absatzes positioniert. |
| LeftMargin | 4 | Gibt an, dass die horizontale Positionierung relativ zum linken Rand der Seite sein soll. |
| RightMargin | 5 | Gibt an, dass die horizontale Positionierung relativ zum rechten Rand der Seite sein soll. |
| InsideMargin | 6 | Gibt an, dass die horizontale Positionierung relativ zum inneren Rand der aktuellen Seite sein soll (der linke Rand bei ungeraden Seiten, der rechte bei geraden Seiten). |
| OutsideMargin | 7 | Gibt an, dass die horizontale Positionierung relativ zum äußeren Rand der aktuellen Seite sein soll (der rechte Rand bei ungeraden Seiten, der linke bei geraden Seiten). |
| Default | n/a | Standardwert ist [Column](./). |


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

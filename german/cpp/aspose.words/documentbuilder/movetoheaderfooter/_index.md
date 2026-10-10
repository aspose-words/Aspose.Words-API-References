---
title: "Aspose::Words::DocumentBuilder::MoveToHeaderFooter Methode"
linktitle: "MoveToHeaderFooter"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::MoveToHeaderFooter-Methode. Bewegt den Cursor zum Anfang einer Kopf‑ oder Fußzeile im aktuellen Abschnitt in C++."
type: docs
weight: 57000
url: /de/cpp/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder::MoveToHeaderFooter method


Bewegt den Cursor zum Anfang einer Kopf‑ oder Fußzeile im aktuellen Abschnitt.

```cpp
void Aspose::Words::DocumentBuilder::MoveToHeaderFooter(Aspose::Words::HeaderFooterType headerFooterType)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | Gibt die Kopf‑ oder Fußzeile an, zu der bewegt werden soll. |
## Hinweise


Nachdem Sie den Cursor in eine Kopf‑ oder Fußzeile verschoben haben, können Sie die übrigen Methoden von [DocumentBuilder](../) verwenden, um den Inhalt der Kopf‑ oder Fußzeile zu ändern.

Wenn Sie für die erste Seite unterschiedliche Kopf‑ und Fußzeilen erstellen möchten, müssen Sie [DifferentFirstPageHeaderFooter](../../pagesetup/get_differentfirstpageheaderfooter/) festlegen.

Wenn Sie für gerade und ungerade Seiten unterschiedliche Kopf‑ und Fußzeilen erstellen möchten, müssen Sie [OddAndEvenPagesHeaderFooter](../../pagesetup/get_oddandevenpagesheaderfooter/) festlegen.

Verwenden Sie [MoveToSection()](../movetosection/), um aus der Kopf‑ oder Fußzeile in den Haupttext zu wechseln.

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

* Enum [HeaderFooterType](../../headerfootertype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Aspose::Words::Rendering::PageInfo Klasse"
linktitle: "PageInfo"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Rendering::PageInfo Klasse. Stellt Informationen über eine bestimmte Dokumentseite dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.rendering/pageinfo/
---
## PageInfo class


Stellt Informationen über eine bestimmte Dokumentseite dar. Weitere Informationen finden Sie im Dokumentationsartikel [Rendering](https://docs.aspose.com/words/cpp/rendering/).

```cpp
class PageInfo : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Colored](./get_colored/)() | Gibt **true** zurück, wenn die Seite farbigen Inhalt enthält. |
| [get_HeightInPoints](./get_heightinpoints/)() | Ermittelt die Höhe der Seite in Punkten. |
| [get_Landscape](./get_landscape/)() const | Gibt **true** zurück, wenn die im Dokument für diese Seite angegebene Ausrichtung Querformat ist. |
| [get_PaperSize](./get_papersize/)() | Ermittelt die Papiergröße als Aufzählung. |
| [get_PaperTray](./get_papertray/)() const | Ermittelt das Papierfach (Bin) für diese Seite, wie im Dokument angegeben. Der Wert ist implementationsspezifisch (Drucker). |
| [get_SizeInPoints](./get_sizeinpoints/)() const | Ermittelt die Seitengröße in Punkten. |
| [get_WidthInPoints](./get_widthinpoints/)() | Ermittelt die Breite der Seite in Punkten. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float) | Berechnet die Seitengröße in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float, float) | Berechnet die Seitengröße in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Hinweise


Die von diesem Objekt zurückgegebene Seitenbreite und -höhe stellen die "endgültige" Größe der Seite dar, d. h. sie sind bereits in die korrekte Ausrichtung gedreht.

## Siehe auch

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)

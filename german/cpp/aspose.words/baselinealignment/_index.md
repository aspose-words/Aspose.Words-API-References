---
title: "Aspose::Words::BaselineAlignment enum"
linktitle: "BaselineAlignment"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BaselineAlignment enum. Gibt die vertikale Position von Schriftarten in einer Zeile in C++ an."
type: docs
weight: 80500
url: /de/cpp/aspose.words/baselinealignment/
---
## BaselineAlignment enum


Gibt die vertikale Position von Schriftarten in einer Zeile an.

```cpp
enum class BaselineAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Oben | 0 | Richtet sich entlang der Oberseite jeder Schriftart aus. |
| Mitte | 1 | Richtet die Mittelpunkte jeder Schriftart aus. |
| Grundlinie | 2 | Richtet sich an der Grundlinie des Absatzes aus. |
| Unten | 3 | Richtet sich an der Unterseite jeder Schriftart aus. |
| Auto | 4 | Die Grundlinie wird automatisch angepasst. |


## Beispiele



Zeigt, wie man die vertikale Position von Schriftarten in einer Zeile festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();
if (format->get_BaselineAlignment() == Aspose::Words::BaselineAlignment::Auto)
{
    format->set_BaselineAlignment(Aspose::Words::BaselineAlignment::Top);
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphBaselineAlignment.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

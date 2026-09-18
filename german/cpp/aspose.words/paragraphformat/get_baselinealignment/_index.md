---
title: "Aspose::Words::ParagraphFormat::get_BaselineAlignment Methode"
linktitle: "get_BaselineAlignment"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_BaselineAlignment Methode. Liest oder setzt die vertikale Position der Schriftart in einer Zeile in C++."
type: docs
weight: 5500
url: /de/cpp/aspose.words/paragraphformat/get_baselinealignment/
---
## ParagraphFormat::get_BaselineAlignment method


Liest oder legt die vertikale Position der Schriftart in einer Zeile fest.

```cpp
Aspose::Words::BaselineAlignment Aspose::Words::ParagraphFormat::get_BaselineAlignment()
```


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

* Enum [BaselineAlignment](../../baselinealignment/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

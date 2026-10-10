---
title: "Aspose::Words::Border::get_ThemeColor Methode"
linktitle: "get_ThemeColor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Border::get_ThemeColor Methode. Gibt die Themenfarbe im angewendeten Farbschema zurück oder legt sie fest, die mit diesem Border-Objekt verknüpft ist, in C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words/border/get_themecolor/
---
## Border::get_ThemeColor method


Liest oder legt die Themenfarbe im angewendeten Farbschema fest, das mit diesem [Border](../)-Objekt verknüpft ist.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Border::get_ThemeColor()
```


## Beispiele



Zeigt, wie man einen Absatz mit einem oberen Rand einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// Setze ThemeColor nur, wenn LineWidth oder LineStyle gesetzt ist.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## Siehe auch

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

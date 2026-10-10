---
title: "Aspose::Words::Border::get_ThemeColor method"
linktitle: "get_ThemeColor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Border::get_ThemeColor method. Ottiene o imposta il colore tematico nello schema di colore applicato associato a questo oggetto Border in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words/border/get_themecolor/
---
## Border::get_ThemeColor method


Ottiene o imposta il colore tematico nello schema di colore applicato associato a questo oggetto [Border](../).

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Border::get_ThemeColor()
```


## Esempi



Mostra come inserire un paragrafo con un bordo superiore.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// Imposta ThemeColor solo quando LineWidth o LineStyle sono impostati.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## Vedi anche

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

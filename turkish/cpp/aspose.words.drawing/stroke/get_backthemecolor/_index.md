---
title: "Aspose::Words::Drawing::Stroke::get_BackThemeColor yöntemi"
linktitle: "get_BackThemeColor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Stroke::get_BackThemeColor yöntemi. Çizgi arka plan rengini temsil eden bir ThemeColor nesnesini alır veya ayarlar (C++ içinde)."
type: docs
weight: 2167
url: /tr/cpp/aspose.words.drawing/stroke/get_backthemecolor/
---
## Stroke::get_BackThemeColor method


Çizgi arka plan rengini temsil eden bir ThemeColor nesnesini alır veya ayarlar.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Stroke::get_BackThemeColor()
```


## Örnekler



Arka tema rengini ve tonlama ve gölgelendirmeyi nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Stroke gradient outline.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);
stroke->set_BackTintAndShade(0.2);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeBackThemeColors.docx");
```

## Ayrıca Bakınız

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

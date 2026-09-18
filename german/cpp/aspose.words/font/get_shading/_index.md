---
title: "Aspose::Words::Font::get_Shading-Methode"
linktitle: "get_Shading"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Shading-Methode. Gibt ein Shading-Objekt zurück, das sich auf die Schattierungsformatierung der Schriftart in C++ bezieht."
type: docs
weight: 34000
url: /de/cpp/aspose.words/font/get_shading/
---
## Font::get_Shading method


Gibt ein [Shading](../../shading/) Objekt zurück, das sich auf die Schattierungsformatierung der Schriftart bezieht.

```cpp
System::SharedPtr<Aspose::Words::Shading> Aspose::Words::Font::get_Shading()
```


## Beispiele



Zeigt, wie Schattierung auf Text angewendet wird, der von einem Document Builder erstellt wurde.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Color(System::Drawing::Color::get_White());

// Eine Möglichkeit, den mit unserer weißen Schriftfarbe erstellten Text sichtbar zu machen
// ist, einen Hintergrundschattierungseffekt anzuwenden.
System::SharedPtr<Aspose::Words::Shading> shading = builder->get_Font()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalUp);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_OrangeRed());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"White text on an orange background with a two-tone texture.");

doc->Save(get_ArtifactsDir() + u"Font.Shading.docx");
```

## Siehe auch

* Class [Shading](../../shading/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

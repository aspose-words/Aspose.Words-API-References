---
title: "Метод Aspose::Words::Font::get_Emboss"
linktitle: "get_Emboss"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_Emboss. Истина, если шрифт отформатирован как рельефный в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words/font/get_emboss/
---
## Font::get_Emboss method


Истина, если шрифт отформатирован как рельефный.

```cpp
bool Aspose::Words::Font::get_Emboss()
```


## Примеры



Показывает, как применять эффекты гравировки/рельефа к тексту.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Color(System::Drawing::Color::get_LightBlue());

// Ниже представлены два способа использования теней для создания 3D‑подобного эффекта текста.
// 1 -  Гравировать текст, чтобы буквы выглядели вдавленными в страницу:
builder->get_Font()->set_Engrave(true);

builder->Writeln(u"This text is engraved.");

// 2 -  Делать рельефный текст, чтобы буквы выглядели выпуклыми из страницы:
builder->get_Font()->set_Engrave(false);
builder->get_Font()->set_Emboss(true);

builder->Writeln(u"This text is embossed.");

doc->Save(get_ArtifactsDir() + u"Font.EngraveEmboss.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

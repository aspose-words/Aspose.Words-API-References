---
title: "Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape method"
linktitle: "get_DisplayBackgroundShape"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape method. Управляет отображением фоновой формы в режиме печатной разметки в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.settings/viewoptions/get_displaybackgroundshape/
---
## ViewOptions::get_DisplayBackgroundShape method


Управляет отображением фоновой фигуры в режиме разметки печати.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape() const
```


## Примеры



Показывает, как скрыть/отобразить фоновые изображения документа в параметрах просмотра.
```cpp
// Используйте строку HTML для создания нового документа с однотонным фоновым цветом.
const System::String html = u"<html>\r\n                <body style='background-color: blue'>\r\n                    <p>Hello world!</p>\r\n                </body>\r\n            </html>";

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_Unicode()->GetBytes(html)));

// Исходный файл документа имеет однотонный фоновый цвет,
// присутствие которого установит флаг "DisplayBackgroundShape" в "true".
ASSERT_TRUE(doc->get_ViewOptions()->get_DisplayBackgroundShape());

// Оставьте "DisplayBackgroundShape" в значении "true", чтобы документ отображал фоновый цвет.
// Это может изменить некоторые цвета текста для улучшения видимости.
// Установите "DisplayBackgroundShape" в "false", чтобы не отображать фоновый цвет.
doc->get_ViewOptions()->set_DisplayBackgroundShape(displayBackgroundShape);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayBackgroundShape.docx");
```

## См. также

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)

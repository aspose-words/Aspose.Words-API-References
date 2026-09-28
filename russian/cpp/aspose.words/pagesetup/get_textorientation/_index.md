---
title: "Метод Aspose::Words::PageSetup::get_TextOrientation"
linktitle: "get_TextOrientation"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::PageSetup::get_TextOrientation. Позволяет задать TextOrientation для всей страницы. Значение по умолчанию — Horizontal в C++."
type: docs
weight: 45000
url: /ru/cpp/aspose.words/pagesetup/get_textorientation/
---
## PageSetup::get_TextOrientation method


Позволяет задать [TextOrientation](./) для всей страницы. Значение по умолчанию — [Horizontal](../../textorientation/)

```cpp
Aspose::Words::TextOrientation Aspose::Words::PageSetup::get_TextOrientation()
```


## Примеры



Показывает, как установить ориентацию текста.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Установите свойство "TextOrientation" в "TextOrientation.Upward", чтобы повернуть весь текст на 90 градусов
// вправо, так что весь текст слева направо теперь будет идти сверху вниз.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TextOrientation(Aspose::Words::TextOrientation::Upward);

doc->Save(get_ArtifactsDir() + u"PageSetup.SetTextOrientation.docx");
```

## См. также

* Enum [TextOrientation](../../textorientation/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

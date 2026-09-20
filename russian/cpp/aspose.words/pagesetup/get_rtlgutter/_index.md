---
title: "Aspose::Words::PageSetup::get_RtlGutter метод"
linktitle: "get_RtlGutter"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PageSetup::get_RtlGutter метод. Получает или задает, использует ли Microsoft Word канавки для раздела в зависимости от языка с направлением справа налево или слева направо в C++."
type: docs
weight: 40000
url: /ru/cpp/aspose.words/pagesetup/get_rtlgutter/
---
## PageSetup::get_RtlGutter method


Получает или задает, использует ли Microsoft Word отступы (gutter) для раздела в зависимости от языка с направлением справа налево или слева направо.

```cpp
bool Aspose::Words::PageSetup::get_RtlGutter()
```


## Примеры



Показывает, как установить поля канвы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Вставьте текст, который охватывает несколько страниц.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
for (int32_t i = 0; i < 6; i++)
{
    builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Канва добавляет пробелы к левому или правому полю страницы,
// что компенсирует центральное сгибание страниц в книге, вторгающееся в макет страницы.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

// Определите, сколько места наши страницы имеют для текста внутри полей, а затем добавьте значение для заполнения поля.
ASSERT_NEAR(470.30, pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin(), 0.01);

pageSetup->set_Gutter(100.0);

// Установите свойство "RtlGutter" в "true", чтобы разместить канву в более подходящем положении для текста справа налево.
pageSetup->set_RtlGutter(true);

// Установите свойство "MultiplePages" в "MultiplePagesType.MirrorMargins", чтобы чередовать
// позицию левого/правого края полей на каждой странице.
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::MirrorMargins);

doc->Save(get_ArtifactsDir() + u"PageSetup.Gutter.docx");
```

## См. также

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

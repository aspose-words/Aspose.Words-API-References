---
title: "Aspose::Words::ParagraphFormat::get_RightIndent метод"
linktitle: "get_RightIndent"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ParagraphFormat::get_RightIndent метод. Получает или задает значение (в пунктах), представляющее правый отступ абзаца в C++."
type: docs
weight: 28000
url: /ru/cpp/aspose.words/paragraphformat/get_rightindent/
---
## ParagraphFormat::get_RightIndent method


Получает или задает значение (в пунктах), представляющее правый отступ абзаца.

```cpp
double Aspose::Words::ParagraphFormat::get_RightIndent()
```


## Примеры



Показывает, как настроить форматирование абзаца для создания текста со смещением от центра.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Центрируйте весь текст, который пишет Document Builder, и настройте отступы.
// Конфигурация отступов ниже создаст блок текста, который будет располагаться асимметрично на странице.
// \"center\", к которому мы выравниваем текст, будет находиться посередине тела текста, а не посередине страницы.
System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
paragraphFormat->set_LeftIndent(100);
paragraphFormat->set_RightIndent(50);
paragraphFormat->set_SpaceAfter(25);

builder->Writeln(u"This paragraph demonstrates how left and right indentation affects word wrapping.");
builder->Writeln(u"The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetParagraphFormatting.docx");
```

## См. также

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

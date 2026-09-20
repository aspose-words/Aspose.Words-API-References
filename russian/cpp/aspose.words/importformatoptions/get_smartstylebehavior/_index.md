---
title: "Метод Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior"
linktitle: "get_SmartStyleBehavior"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior. Получает или задает логическое значение, определяющее, как стили будут импортироваться, когда они имеют одинаковые имена в исходных и целевых документах. Значение по умолчанию — false в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words/importformatoptions/get_smartstylebehavior/
---
## ImportFormatOptions::get_SmartStyleBehavior method


Получает или задает логическое значение, которое определяет, как стили будут импортированы, когда они имеют одинаковые имена в исходных и целевых документах. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior() const
```

## Примечания


Когда эта опция **enabled**, исходный стиль будет расширен в прямые атрибуты внутри целевого документа, если используется режим импорта [KeepSourceFormatting](../../importformatmode/).

Когда эта опция **disabled**, исходный стиль будет расширен только если он нумерован. Существующие атрибуты целевого документа не будут переопределены, включая списки.

## Примеры



Показывает, как разрешать дублирующиеся стили при вставке документов.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

System::SharedPtr<Aspose::Words::Style> myStyle = builder->get_Document()->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

// Клонируйте документ и отредактируйте стиль "MyStyle" клона, чтобы он имел другой цвет, чем у оригинала.
// Если вставить клон в оригинальный документ, два стиля с одинаковым именем вызовут конфликт.
System::SharedPtr<Aspose::Words::Document> srcDoc = dstDoc->Clone();
srcDoc->get_Styles()->idx_get(u"MyStyle")->get_Font()->set_Color(System::Drawing::Color::get_Red());

// Когда мы включаем SmartStyleBehavior и используем режим импорта KeepSourceFormatting,
// Aspose.Words разрешит конфликты стилей, преобразуя стили исходного документа.
// с теми же именами, что и стили назначения, в прямые атрибуты абзаца.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_SmartStyleBehavior(true);

builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.SmartStyleBehavior.docx");
```

## См. также

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

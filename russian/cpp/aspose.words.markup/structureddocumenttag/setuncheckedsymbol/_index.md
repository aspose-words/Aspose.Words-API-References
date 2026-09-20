---
title: "Aspose::Words::Markup::StructuredDocumentTag::SetUncheckedSymbol метод"
linktitle: "SetUncheckedSymbol"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::SetUncheckedSymbol метод. Устанавливает символ, используемый для представления состояния снятия галочки в элементе управления содержимым флажка в C++."
type: docs
weight: 59000
url: /ru/cpp/aspose.words.markup/structureddocumenttag/setuncheckedsymbol/
---
## StructuredDocumentTag::SetUncheckedSymbol method


Устанавливает символ, используемый для представления неотмеченного состояния элемента управления checkbox.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::SetUncheckedSymbol(int32_t characterCode, const System::String &fontName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| characterCode | int32_t | Код символа для указанного знака. |
| fontName | const System::String\& | Имя шрифта, содержащего символ. |
## Примечания


Вызов этого метода будет работать только для типов SDT [Checkbox](../../sdttype/).

Для всех остальных типов SDT будет возникать исключение.

## Примеры



Показать, как создать структурный тег документа в виде флажка.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto sdtCheckBox = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
sdtCheckBox->set_Checked(true);

// Мы можем задать символы, используемые для отображения состояния отмечено/не отмечено в элементе управления содержимым флажка.
sdtCheckBox->SetCheckedSymbol(0x00A9, u"Times New Roman");
sdtCheckBox->SetUncheckedSymbol(0x00AE, u"Times New Roman");

builder->InsertNode(sdtCheckBox);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CheckBox.docx");
```

## См. также

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)

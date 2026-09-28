---
title: "Метод Aspose::Words::Markup::StructuredDocumentTag::get_Checked"
linktitle: "get_Checked"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Markup::StructuredDocumentTag::get_Checked. Получает/устанавливает текущее состояние флажка SDT. Значение по умолчанию для этого свойства — false в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.markup/structureddocumenttag/get_checked/
---
## StructuredDocumentTag::get_Checked method


Получает/устанавливает текущее состояние флажка **SDT**. Значение по умолчанию для этого свойства — **false**.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_Checked()
```

## Примечания


Доступ к этому свойству будет работать только для типов SDT [Checkbox](../../sdttype/).

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

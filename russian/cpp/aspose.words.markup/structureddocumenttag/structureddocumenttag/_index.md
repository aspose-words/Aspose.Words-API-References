---
title: "Конструктор Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag"
linktitle: "StructuredDocumentTag"
second_title: "Справочник API Aspose.Words для C++"
description: "Конструктор Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag. Инициализирует новый экземпляр класса Structured document tag в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.markup/structureddocumenttag/structureddocumenttag/
---
## StructuredDocumentTag::StructuredDocumentTag constructor


Инициализирует новый экземпляр класса **Structured document tag**.

```cpp
Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Markup::SdtType type, Aspose::Words::Markup::MarkupLevel level)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| док | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Документ‑владелец. |
| тип | Aspose::Words::Markup::SdtType | Тип узла SDT. |
| уровень | Aspose::Words::Markup::MarkupLevel | Уровень узла SDT в документе. |
## Примечания


Можно создать следующие типы SDT:

* [Checkbox](../../sdttype/)
* [DropDownList](../../sdttype/)
* [ComboBox](../../sdttype/)
* [Date](../../sdttype/)
* [BuildingBlockGallery](../../sdttype/)
* [Group](../../sdttype/)
* [Picture](../../sdttype/)
* [RichText](../../sdttype/)
* [PlainText](../../sdttype/)



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

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [SdtType](../../sdttype/)
* Enum [MarkupLevel](../../markuplevel/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)

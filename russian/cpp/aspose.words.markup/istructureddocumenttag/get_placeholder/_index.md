---
title: "Метод Aspose::Words::Markup::IStructuredDocumentTag::get_Placeholder"
linktitle: "get_Placeholder"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Markup::IStructuredDocumentTag::get_Placeholder. Возвращает BuildingBlock, содержащий текст-заполнитель, который должен отображаться, когда содержимое этого SDT пусто, соответствующий сопоставленный элемент XML пуст, как указано в элементе XmlMapping, или элемент IsShowingPlaceholderText установлен в true в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.markup/istructureddocumenttag/get_placeholder/
---
## IStructuredDocumentTag::get_Placeholder method


Возвращает [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) содержащий текст-заполнитель, который должен отображаться, когда содержимое этого SDT пусто, соответствующий сопоставленный элемент XML пуст, как указано в элементе [XmlMapping](../get_xmlmapping/), или элемент [IsShowingPlaceholderText](../get_isshowingplaceholdertext/) установлен в true.

```cpp
virtual System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::Markup::IStructuredDocumentTag::get_Placeholder()=0
```


## Примеры



Показывает, как использовать содержимое строительного блока в качестве пользовательского текста-заполнителя для структурированного тега документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Вставьте структурированный тег документа простого текста типа "PlainText", который будет работать как текстовое поле.
// Содержимое, которое он будет отображать по умолчанию, — подсказка "Click here to enter text.".
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Мы можем заставить тег отображать содержимое строительного блока вместо текста по умолчанию.
// Сначала добавьте строительный блок с содержимым в документ глоссария.
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();

auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"Custom Placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(glossaryDoc));
substituteBlock->get_FirstSection()->get_Body()->AppendParagraph(u"Custom placeholder text.");

glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// Затем используйте свойство "PlaceholderName" структурированного тега документа, чтобы сослаться на этот строительный блок по имени.
tag->set_PlaceholderName(u"Custom Placeholder");

// Если "PlaceholderName" ссылается на существующий блок в глоссарии родительского документа,
// мы сможем проверить строительный блок через свойство "Placeholder".
ASPOSE_ASSERT_EQ(substituteBlock, tag->get_Placeholder());

// Установите свойство "IsShowingPlaceholderText" в значение "true", чтобы рассматривать
// текущие содержимое структурированного тега документа как текст-заполнитель.
// Это означает, что щелчок по текстовому полю в Microsoft Word сразу выделит всё содержимое тега.
// Установите свойство "IsShowingPlaceholderText" в значение "false", чтобы получить
// структурированный тег, чтобы рассматривать его содержимое как уже введённый пользователем текст.
// Щелчок по этому тексту в Microsoft Word разместит мигающий курсор в месте щелчка.
tag->set_IsShowingPlaceholderText(isShowingPlaceholderText);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

## См. также

* Class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)

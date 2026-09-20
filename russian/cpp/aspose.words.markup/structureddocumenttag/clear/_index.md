---
title: "Aspose::Words::Markup::StructuredDocumentTag::Clear метод"
linktitle: "Clear"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::Clear метод. Очищает содержимое этого структурированного тега документа и отображает заполнитель, если он определён в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag::Clear method


Очищает содержимое этого структурированного тега документа и отображает заполнитель, если он определён.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::Clear()
```

## Примечания


Невозможно очистить содержимое структурированного тега документа, если у него есть правки.

Если этот структурированный тег документа сопоставлен с пользовательским XML (с использованием свойства [XmlMapping](../get_xmlmapping/)), ссылка на узел XML будет очищена.

## Примеры



Показывает, как удалить содержимое элементов структурированного тега документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Создайте структурированный тег документа с простым текстом, а затем добавьте его в документ.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// Этот структурированный тег документа, представленный в виде текстового поля, уже отображает текст заполнителя.
ASSERT_EQ(u"Click here to enter text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// Создайте блок-сборки с текстовым содержимым.
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();
auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"My placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->EnsureMinimum();
substituteBlock->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(glossaryDoc, u"Custom placeholder text."));
glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// Установите свойство "PlaceholderName" структурированного тега документа в имя нашего блока-сборки, чтобы получить
// структурированный тег документа отображал содержимое блока-сборки вместо оригинального текста по умолчанию.
tag->set_PlaceholderName(u"My placeholder");

ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// Отредактируйте текст структурированного тега документа и скройте текст заполнителя.
auto run = System::ExplicitCast<Aspose::Words::Run>(tag->GetChild(Aspose::Words::NodeType::Run, 0, true));
run->set_Text(u"New text.");
tag->set_IsShowingPlaceholderText(false);

ASSERT_EQ(u"New text.", tag->GetText().Trim());

// Используйте метод "Clear", чтобы очистить содержимое этого структурированного тега документа и снова отобразить заполнитель.
tag->Clear();

ASSERT_TRUE(tag->get_IsShowingPlaceholderText());
ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
```

## См. также

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)

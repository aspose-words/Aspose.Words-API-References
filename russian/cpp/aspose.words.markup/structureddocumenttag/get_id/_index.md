---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_Id method"
linktitle: "get_Id"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_Id method. Указывает уникальный только для чтения постоянный числовой Id для этого SDT в C++."
type: docs
weight: 17000
url: /ru/cpp/aspose.words.markup/structureddocumenttag/get_id/
---
## StructuredDocumentTag::get_Id method


Указывает уникальный только для чтения постоянный числовой идентификатор для этого **SDT**.

```cpp
int32_t Aspose::Words::Markup::StructuredDocumentTag::get_Id() override
```

## Примечания


Атрибут Id должен соответствовать следующим правилам:* Документ будет сохранять идентификаторы SDT только в том случае, если весь документ клонируется [Clone](../../../aspose.words/document/clone/).
* During [ImportNode()](../) Id shall be retained if import does not cause conflicts with other SDT Ids in the target document.
* If multiple SDT nodes specify the same decimal number value for the Id attribute, then the first SDT in the document shall maintain this original Id, and all subsequent SDT nodes shall have new identifiers assigned to them when the document is loaded.
* During standalone SDT [Clone()](../) operation new unique ID will be generated for the cloned SDT node.
* If Id is not specified in the source document, then the SDT node shall have a new unique identifier assigned to it when the document is loaded.



## Примеры



Показывает, как создать структурированный тег документа в обычном текстовом поле и изменить его внешний вид.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Создайте структурированный тег документа, который будет содержать обычный текст.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Установите заголовок и цвет рамки, которая появляется при наведении мыши на структурированный тег документа в Microsoft Word.
tag->set_Title(u"My plain text");
tag->set_Color(System::Drawing::Color::get_Magenta());

// Установите тег для этого структурированного тега документа, который можно получить
// в виде XML‑элемента с именем "tag", со строкой ниже в его атрибуте "@val".
tag->set_Tag(u"MyPlainTextSDT");

// Каждый структурированный тег документа имеет случайный уникальный ID.
ASSERT_TRUE(tag->get_Id() > 0);

// Установите шрифт для текста внутри структурированного тега документа.
tag->get_ContentsFont()->set_Name(u"Arial");

// Установите шрифт для текста в конце структурированного тега документа.
// Любой текст, который мы вводим в теле документа после выхода из тега с помощью клавиш со стрелками, будет использовать этот шрифт.
tag->get_EndCharacterFont()->set_Name(u"Arial Black");

// По умолчанию это false, и нажатие Enter внутри структурированного тега документа ничего не делает.
// Если установить значение true, наш структурированный тег документа может содержать несколько строк.

// Установите свойство "Multiline" в "false", чтобы разрешить содержимое только
// для этого структурированного тега документа в одну строку.
// Установите свойство "Multiline" в "true", чтобы тег мог содержать несколько строк контента.
tag->set_Multiline(true);

// Установите свойство "Appearance" в "SdtAppearance.Tags", чтобы отображать теги вокруг содержимого.
// По умолчанию структурный тег документа отображается как BoundingBox.
tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

// Вставьте клон нашего структурного тега документа в новый абзац.
auto tagClone = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(System::ExplicitCast<Aspose::Words::Node>(tag)->Clone(true));
builder->InsertParagraph();
builder->InsertNode(tagClone);

// Используйте метод "RemoveSelfOnly", чтобы удалить структурный тег документа, при этом сохранив его содержимое в документе.
tagClone->RemoveSelfOnly();

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlainText.docx");
```

## См. также

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)

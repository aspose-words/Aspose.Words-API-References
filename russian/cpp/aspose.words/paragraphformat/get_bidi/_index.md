---
title: "Aspose::Words::ParagraphFormat::get_Bidi метод"
linktitle: "get_Bidi"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ParagraphFormat::get_Bidi метод. Получает или задает, является ли этот абзац направлением справа налево в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words/paragraphformat/get_bidi/
---
## ParagraphFormat::get_Bidi method


Получает или задает, является ли этот абзац направленным справа налево.

```cpp
bool Aspose::Words::ParagraphFormat::get_Bidi()
```

## Примечания


Когда **true**, фрагменты и другие встроенные объекты в этом абзаце располагаются справа налево.

## Примеры



Показывает, как создавать совместимые с языками справа налево списки с полями BIDIOUTLINE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Поле BIDIOUTLINE нумерует абзацы как поля AUTONUM/LISTNUM,
// но отображается только когда включён язык редактирования справа налево, например иврит или арабский.
// Следующее поле отобразит ".1", RTL-эквивалент номера списка "1.".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBidiOutline>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true));
builder->Writeln(u"שלום");

ASSERT_EQ(u" BIDIOUTLINE ", field->GetFieldCode());

// Добавьте ещё два поля BIDIOUTLINE, которые отобразят ".2" и ".3".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");

// Установите горизонтальное выравнивание текста для каждого абзаца в документе в RTL.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    para->get_ParagraphFormat()->set_Bidi(true);
}

// Если включить язык редактирования справа налево в Microsoft Word, наши поля будут отображать числа.
// В противном случае они отобразят "###".
doc->Save(get_ArtifactsDir() + u"Field.BIDIOUTLINE.docx");
```


Показывает, как определить направление текста в простом документе.
```cpp
// Создайте объект "TxtLoadOptions", который можно передать конструктору документа
// чтобы изменить способ загрузки простого документа.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Установите свойство "DocumentDirection" в "DocumentDirection.Auto" для автоматического определения
// направления каждого абзаца текста, который Aspose.Words загружает из простого текста.
// Свойство "Bidi" каждого абзаца будет хранить его направление.
loadOptions->set_DocumentDirection(Aspose::Words::Loading::DocumentDirection::Auto);

// Определять иврит как направление справа налево.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// Определять английский как направление справа налево.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```

## См. также

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

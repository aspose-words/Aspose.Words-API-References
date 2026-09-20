---
title: "Aspose::Words::Fields::FieldShape::get_Text метод"
linktitle: "get_Text"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldShape::get_Text метод. Получает или задает текст для получения в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldshape/get_text/
---
## FieldShape::get_Text method


Получает или задает текст для получения.

```cpp
System::String Aspose::Words::Fields::FieldShape::get_Text()
```


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


Показывает, как некоторые старые поля Microsoft Word, такие как SHAPE и EMBED, обрабатываются при загрузке.
```cpp
// Откройте документ, созданный в Microsoft Word 2003.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy fields.doc");

// Если открыть документ Word и нажать Alt+F9, мы увидим поле SHAPE и поле EMBED.
// Поле SHAPE служит якорем/холстом для объекта AutoShape с включённым стилем обтекания «В строке с текстом».
// Поле EMBED имеет ту же функцию, но для встроенного объекта,
// например, таблицы из внешнего документа Excel.
// Однако эти поля не появятся в коллекции Fields документа.
ASSERT_EQ(0, doc->get_Range()->get_Fields()->get_Count());

// Эти поля поддерживаются только старыми версиями Microsoft Word.
// Процесс загрузки документа преобразует эти поля в объекты Shape,
// к которым мы можем получить доступ в коллекции узлов документа.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);
ASSERT_EQ(3, shapes->get_Count());

// Первый узел Shape соответствует полю SHAPE во входном документе,
// который является встроенным холстом для AutoShape.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(0));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Image, shape->get_ShapeType());

// Второй узел Shape — это сам AutoShape.
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(1));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Can, shape->get_ShapeType());

// Третий Shape — это то, что было полем EMBED, содержащим внешнюю таблицу.
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(2));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::OleObject, shape->get_ShapeType());
```

## См. также

* Class [FieldShape](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)

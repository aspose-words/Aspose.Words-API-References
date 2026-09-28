---
title: "Aspose::Words::Style class"
linktitle: "Style"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Style class. Представляет один встроенный или пользовательский стиль. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 64000
url: /ru/cpp/aspose.words/style/
---
## Style class


Представляет один встроенный или пользовательский стиль. Чтобы узнать больше, посетите статью документации [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class Style : public Aspose::Words::IParaAttrSource,
              public Aspose::Words::IRunAttrSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Сравнивает с указанным стилем. Styles Istds сравниваются только для встроенных стилей. Значения по умолчанию стилей не включаются в сравнение. Базовый стиль, связанный стиль и стиль следующего абзаца сравниваются рекурсивно. |
| [get_Aliases](./get_aliases/)() | Получает все псевдонимы этого стиля. Если у стиля нет псевдонимов, возвращается пустой массив строк. |
| [get_AutomaticallyUpdate](./get_automaticallyupdate/)() const | Указывает, переопределяется ли этот стиль автоматически на основе соответствующего значения. |
| [get_BaseStyleName](./get_basestylename/)() | Получает/устанавливает имя стиля, на котором основан этот стиль. |
| [get_BuiltIn](./get_builtin/)() | True, если этот стиль является одним из встроенных стилей в MS Word. |
| [get_Document](./get_document/)() | Получает документ‑владельца. |
| [get_Font](./get_font/)() | Получает символьное форматирование стиля. |
| [get_IsHeading](./get_isheading/)() | True, когда стиль является одним из встроенных стилей Heading. |
| [get_IsQuickStyle](./get_isquickstyle/)() const | Указывает, отображается ли этот стиль в быстрой галерее [Style](./) внутри пользовательского интерфейса MS Word. |
| [get_LinkedStyleName](./get_linkedstylename/)() | Получает/устанавливает имя [Style](./), связанного с этим. Возвращает пустую строку, если стили не связаны. |
| [get_List](./get_list/)() | Получает список, определяющий форматирование этого стиля списка. |
| [get_ListFormat](./get_listformat/)() | Обеспечивает доступ к свойствам форматирования списка стиля абзаца. |
| [get_Locked](./get_locked/)() const | Указывает, заблокирован ли этот стиль. |
| [get_Name](./get_name/)() const | Получает или устанавливает имя стиля. |
| [get_NextParagraphStyleName](./get_nextparagraphstylename/)() | Получает/устанавливает имя стиля, который будет автоматически применяться к новому абзацу, вставленному после абзаца, отформатированного указанным стилем. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Получает форматирование абзаца стиля. |
| [get_Priority](./get_priority/)() const | Получает/устанавливает целочисленное значение, представляющее приоритет сортировки стилей в панели задач Styles. |
| [get_SemiHidden](./get_semihidden/)() const | Получает/устанавливает, скрывается ли стиль в галерее Стилей и на панели задач Стилей. |
| [get_StyleIdentifier](./get_styleidentifier/)() const | Получает независимый от локали идентификатор стиля для встроенного стиля. |
| [get_Styles](./get_styles/)() const | Получает коллекцию стилей, к которым принадлежит этот стиль. |
| [get_Type](./get_type/)() const | Получает тип стиля (абзацный или символьный). |
| [get_UnhideWhenUsed](./get_unhidewhenused/)() const | Получает/устанавливает, отображается ли используемый в текущем документе стиль в галерее Стилей и на панели задач Стилей. Истина, когда используемый стиль должен отображаться в галерее Стилей. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Удаляет указанный стиль из документа. |
| [set_AutomaticallyUpdate](./set_automaticallyupdate/)(bool) | Сеттер для [Aspose::Words::Style::get_AutomaticallyUpdate](./get_automaticallyupdate/). |
| [set_BaseStyleName](./set_basestylename/)(const System::String\&) | Сеттер для [Aspose::Words::Style::get_BaseStyleName](./get_basestylename/). |
| [set_IsQuickStyle](./set_isquickstyle/)(bool) | Сеттер для [Aspose::Words::Style::get_IsQuickStyle](./get_isquickstyle/). |
| [set_LinkedStyleName](./set_linkedstylename/)(const System::String\&) | Сеттер для [Aspose::Words::Style::get_LinkedStyleName](./get_linkedstylename/). |
| [set_Locked](./set_locked/)(bool) | Сеттер для [Aspose::Words::Style::get_Locked](./get_locked/). |
| [set_Name](./set_name/)(const System::String\&) | Сеттер для [Aspose::Words::Style::get_Name](./get_name/). |
| [set_NextParagraphStyleName](./set_nextparagraphstylename/)(const System::String\&) | Сеттер для [Aspose::Words::Style::get_NextParagraphStyleName](./get_nextparagraphstylename/). |
| [set_Priority](./set_priority/)(int32_t) | Сеттер для [Aspose::Words::Style::get_Priority](./get_priority/). |
| [set_SemiHidden](./set_semihidden/)(bool) | Сеттер для [Aspose::Words::Style::get_SemiHidden](./get_semihidden/). |
| [set_UnhideWhenUsed](./set_unhidewhenused/)(bool) | Сеттер для [Aspose::Words::Style::get_UnhideWhenUsed](./get_unhidewhenused/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как создать и применить пользовательский стиль.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
// Автоматически переопределить стиль.
style->set_AutomaticallyUpdate(true);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Примените один из стилей документа к абзацу, который создает DocumentBuilder.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// Удалите наш пользовательский стиль из коллекции стилей документа.
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// Любой текст, использующий удалённый стиль, возвращается к форматированию по умолчанию.
ASSERT_FALSE(doc->get_Styles()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Style>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Style> s)>>([](System::SharedPtr<Aspose::Words::Style> s) -> bool
{
    return s->get_Name() == u"MyStyle";
}))));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```


Показывает, как создать и использовать абзацный стиль со списковой разметкой.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте пользовательский абзацный стиль.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Создайте список и убедитесь, что абзацы, использующие этот стиль, будут использовать этот список.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Примените абзацный стиль к текущему абзацу DocumentBuilder, а затем добавьте некоторый текст.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Измените стиль DocumentBuilder на такой, который не содержит форматирования списка, и напишите еще один абзац.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

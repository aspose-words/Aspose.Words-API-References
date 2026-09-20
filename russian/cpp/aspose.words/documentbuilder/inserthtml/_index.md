---
title: "Aspose::Words::DocumentBuilder::InsertHtml метод"
linktitle: "InsertHtml"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::InsertHtml метод. Вставляет строку HTML в документ на C++."
type: docs
weight: 37000
url: /ru/cpp/aspose.words/documentbuilder/inserthtml/
---
## DocumentBuilder::InsertHtml(const System::String\&) method


Вставляет строку HTML в документ.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| HTML | const System::String\& | HTML‑строка для вставки в документ. |

## Примеры



Показывает, как использовать конструктор документа для вставки HTML‑контента в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const System::String html = System::String(u"<p align='right'>Paragraph right</p>") + u"<b>Implicit paragraph left</b>" + u"<div align='center'>Div center</div>" + u"<h1 align='left'>Heading 1 left.</h1>";

builder->InsertHtml(html);

// Вставка HTML‑кода анализирует форматирование каждого элемента и преобразует его в эквивалентное форматирование текста документа.
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(u"Paragraph right", paragraphs->idx_get(0)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());

ASSERT_EQ(u"Implicit paragraph left", paragraphs->idx_get(1)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_TRUE(paragraphs->idx_get(1)->get_Runs()->idx_get(0)->get_Font()->get_Bold());

ASSERT_EQ(u"Div center", paragraphs->idx_get(2)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Center, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

ASSERT_EQ(u"Heading 1 left.", paragraphs->idx_get(3)->GetText().Trim());
ASSERT_EQ(u"Heading 1", paragraphs->idx_get(3)->get_ParagraphFormat()->get_Style()->get_Name());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHtml.docx");
```

## См. также

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, Aspose::Words::HtmlInsertOptions) method


Вставляет строку HTML в документ. Позволяет указать дополнительные параметры.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, Aspose::Words::HtmlInsertOptions options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| HTML | const System::String\& | HTML‑строка для вставки в документ. |
| параметры | Aspose::Words::HtmlInsertOptions | Параметры, используемые при вставке строки HTML. |

## См. также

* Enum [HtmlInsertOptions](../../htmlinsertoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, bool) method


Вставляет строку HTML в документ.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, bool useBuilderFormatting)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| HTML | const System::String\& | HTML‑строка для вставки в документ. |
| useBuilderFormatting | bool | Значение, указывающее, используется ли форматирование, указанное в [DocumentBuilder](../), в качестве базового форматирования для текста, импортированного из HTML. |
## Примечания


Вы можете использовать этот метод для вставки фрагмента HTML или целого HTML‑документа.

Когда *useBuilderFormatting* равно **false**, форматирование [DocumentBuilder](../) игнорируется, и форматирование вставленного текста основывается на форматировании HTML по умолчанию. В результате текст выглядит так, как он отображается в браузерах.

Когда *useBuilderFormatting* равно **true**, форматирование вставленного текста основывается на форматировании [DocumentBuilder](../), и текст выглядит так, как будто он был вставлен с помощью [Write()](../).

## Примеры



Показывает, как применить форматирование конструктора документа при вставке HTML‑контента.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Установите выравнивание текста для конструктора, вставьте HTML‑абзац с указанным выравниванием и один без него.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Distributed);
builder->InsertHtml(System::String(u"<p align='right'>Paragraph 1.</p>") + u"<p>Paragraph 2.</p>", useBuilderFormatting);

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// В первом абзаце указано выравнивание. Когда InsertHtml анализирует HTML‑код,
// значение выравнивания абзаца, найденное в HTML‑коде, всегда переопределяет значение конструктора документа.
ASSERT_EQ(u"Paragraph 1.", paragraphs->idx_get(0)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());

// Во втором абзаце выравнивание не указано. Его значение выравнивания может быть заполнено
// значением конструктора в зависимости от флага, переданного в метод InsertHtml.
ASSERT_EQ(u"Paragraph 2.", paragraphs->idx_get(1)->GetText().Trim());
ASSERT_EQ(useBuilderFormatting ? Aspose::Words::ParagraphAlignment::Distributed : Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHtmlWithFormatting.docx");
```

## См. также

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

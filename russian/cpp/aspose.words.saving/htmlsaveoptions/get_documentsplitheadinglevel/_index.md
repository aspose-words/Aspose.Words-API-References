---
title: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel"
linktitle: "get_DocumentSplitHeadingLevel"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel. Указывает максимальный уровень заголовков, при котором документ будет разделён. Значение по умолчанию — %2 в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitheadinglevel/
---
## HtmlSaveOptions::get_DocumentSplitHeadingLevel method


Указывает максимальный уровень заголовков, при котором документ разбивается. Значение по умолчанию — **%2**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel() const
```

## Примечания


Когда [DocumentSplitCriteria](../get_documentsplitcriteria/) включает [HeadingParagraph](../../documentsplitcriteria/) и это свойство установлено в значение от 1 до 9, документ будет разделён по абзацам, отформатированным стилями **Heading 1**, **Heading 2**, **Heading 3** и т.д. до указанного уровня заголовка.

По умолчанию только абзацы с **Heading 1** и **Heading 2** вызывают разделение документа. Установка этого свойства в ноль приведёт к тому, что документ не будет разделяться по абзацам‑заголовкам вовсе.

## Примеры



Показывает, как разделить результирующий HTML‑документ по заголовкам на несколько частей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Каждый абзац, отформатированный с помощью стиля "Heading", может служить заголовком.
// Каждый заголовок также может иметь уровень, определяемый номером его стиля заголовка.
// Ниже приведённые заголовки имеют уровни 1‑3.
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #1");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #2");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #3");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #4");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #5");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #6");

// Создайте объект HtmlSaveOptions и задайте критерий разделения "HeadingParagraph".
// Эти критерии разделят документ по абзацам со стилями "Heading" на несколько более мелких документов,
// и сохранят каждый документ в отдельный HTML‑файл в локальной файловой системе.
// Мы также зададим максимальный уровень заголовка, при котором документ будет разделён до уровня 2.
// Сохранение документа разделит его по заголовкам уровней 1 и 2, но не по уровням от 3 до 9.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);
options->set_DocumentSplitHeadingLevel(2);

// В нашем документе четыре заголовка уровней 1‑2. Один из этих заголовков не будет
// точкой разбиения, поскольку он находится в начале документа.
// Операция сохранения разделит наш документ в трёх местах, получив четыре более мелких документа.
doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html");

ASSERT_EQ(u"Heading #1", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-01.html");

ASSERT_EQ(System::String(u"Heading #2\r") + u"Heading #3", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-02.html");

ASSERT_EQ(u"Heading #4", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-03.html");

ASSERT_EQ(System::String(u"Heading #5\r") + u"Heading #6", doc->GetText().Trim());
```

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

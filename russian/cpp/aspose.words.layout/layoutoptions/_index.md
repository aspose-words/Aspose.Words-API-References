---
title: "Класс Aspose::Words::Layout::LayoutOptions"
linktitle: "LayoutOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Layout::LayoutOptions. Содержит параметры, позволяющие управлять процессом компоновки документа. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.layout/layoutoptions/
---
## LayoutOptions class


Содержит параметры, позволяющие управлять процессом компоновки документа. Чтобы узнать больше, посетите статью документации [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Callback](./get_callback/)() const | Получает реализацию [IPageLayoutCallback](../ipagelayoutcallback/), используемую моделью компоновки страниц. |
| [get_CommentDisplayMode](./get_commentdisplaymode/)() const | Получает или задает способ отображения комментариев. Значение по умолчанию — [ShowInBalloons](../commentdisplaymode/). |
| [get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/)() const | Получает или задает режим поведения при вычислении номеров страниц, когда непрерывный раздел перезапускает нумерацию страниц. |
| [get_IgnorePrinterMetrics](./get_ignoreprintermetrics/)() const | Получает или задает индикатор того, игнорируется ли параметр совместимости «Использовать метрики принтера для компоновки документа». По умолчанию **true**. |
| [get_KeepOriginalFontMetrics](./get_keeporiginalfontmetrics/)() const | Получает или задает индикатор того, следует ли использовать оригинальные метрики шрифта после подстановки шрифта. По умолчанию **true**. |
| [get_RevisionOptions](./get_revisionoptions/)() const | Получает параметры ревизии. |
| [get_ShowHiddenText](./get_showhiddentext/)() const | Получает или задает индикатор того, отображается ли скрытый текст в документе. По умолчанию **false**. |
| [get_ShowParagraphMarks](./get_showparagraphmarks/)() const | Получает или задает индикатор того, отображаются ли знаки абзаца. По умолчанию **false**. |
| [get_TextShaperFactory](./get_textshaperfactory/)() const | Получает реализацию [ITextShaperFactory](../), используемую для функций рендеринга продвинутой типографии. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutOptions](./layoutoptions/)() |  |
| [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::Layout::IPageLayoutCallback\>\&) | Задает реализацию [IPageLayoutCallback](../ipagelayoutcallback/), используемую моделью компоновки страниц. |
| [set_CommentDisplayMode](./set_commentdisplaymode/)(Aspose::Words::Layout::CommentDisplayMode) | Сеттер для [Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode](./get_commentdisplaymode/). |
| [set_ContinuousSectionPageNumberingRestart](./set_continuoussectionpagenumberingrestart/)(Aspose::Words::Layout::ContinuousSectionRestart) | Сеттер для [Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/). |
| [set_IgnorePrinterMetrics](./set_ignoreprintermetrics/)(bool) | Сеттер для [Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics](./get_ignoreprintermetrics/). |
| [set_KeepOriginalFontMetrics](./set_keeporiginalfontmetrics/)(bool) | Сеттер для [Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics](./get_keeporiginalfontmetrics/). |
| [set_ShowHiddenText](./set_showhiddentext/)(bool) | Сеттер для [Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText](./get_showhiddentext/). |
| [set_ShowParagraphMarks](./set_showparagraphmarks/)(bool) | Сеттер для [Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks](./get_showparagraphmarks/). |
| [set_TextShaperFactory](./set_textshaperfactory/)(const System::SharedPtr\<Aspose::Words::Shaping::ITextShaperFactory\>\&) | Задает реализацию [ITextShaperFactory](../), используемую для функций рендеринга продвинутой типографии. |
| static [Type](./type/)() |  |
## Примечания


Вы не создаёте экземпляры этого класса напрямую. Используйте свойство [LayoutOptions](../../aspose.words/document/get_layoutoptions/), чтобы получить параметры компоновки для этого документа.

Обратите внимание, что после изменения любых параметров, присутствующих в этом классе, следует вызвать метод [UpdatePageLayout](../../aspose.words/document/updatepagelayout/), чтобы применить изменённые параметры к компоновке.

## Примеры



Показывает, как скрыть текст в отрендеренном выходном документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте скрытый текст, затем укажите, хотим ли мы опустить его в отрендеренном документе.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```


Показывает, как отобразить знаки абзацев в отрендеренном выходном документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Добавьте несколько абзацев, затем включите отображение знаков абзацев, чтобы показать конец абзацев
// с символом абзацного знака (¶) при рендеринге документа.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```


Показывает, как изменить внешний вид правок в отрендеренном выходном документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте правку, затем измените цвет всех правок на зелёный.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Удалите полосу, которая появляется слева от каждой исправленной строки.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## См. также

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)

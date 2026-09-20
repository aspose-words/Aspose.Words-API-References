---
title: "Класс Aspose::Words::PageSetup"
linktitle: "PageSetup"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::PageSetup. Представляет свойства настройки страницы раздела. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 46000
url: /ru/cpp/aspose.words/pagesetup/
---
## PageSetup class


Представляет свойства настройки страницы секции. Чтобы узнать больше, посетите статью документации [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class PageSetup : public Aspose::Words::IBorderAttrSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Сбрасывает настройки страницы к размерам бумаги, полям и ориентации по умолчанию. |
| [get_Bidi](./get_bidi/)() | Указывает, что этот раздел содержит двунаправленный (сложные скрипты) текст. |
| [get_BorderAlwaysInFront](./get_borderalwaysinfront/)() | Указывает, где граница страницы расположена относительно пересекающихся текстов и объектов. |
| [get_BorderAppliesTo](./get_borderappliesto/)() | Указывает, на каких страницах печатается граница страницы. |
| [get_BorderDistanceFrom](./get_borderdistancefrom/)() | Получает или задает значение, указывающее, измеряется ли указанная граница страницы от края страницы или от окружающего её текста. |
| [get_Borders](./get_borders/)() | Получает коллекцию границ страницы. |
| [get_BorderSurroundsFooter](./get_bordersurroundsfooter/)() | Указывает, включает ли граница страницы нижний колонтитул или исключает его. |
| [get_BorderSurroundsHeader](./get_bordersurroundsheader/)() | Указывает, включает ли граница страницы верхний колонтитул или исключает его. |
| [get_BottomMargin](./get_bottommargin/)() | Возвращает или задает расстояние (в пунктах) между нижним краем страницы и нижней границей основного текста. |
| [get_ChapterPageSeparator](./get_chapterpageseparator/)() | Получает или задает символ-разделитель, который появляется между номером главы и номером страницы. |
| [get_CharactersPerLine](./get_charactersperline/)() | Получает или задает количество символов в строке сетки документа. |
| [get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/)() | Истина, если на первой странице используется другой верхний или нижний колонтитул. |
| [get_EndnoteOptions](./get_endnoteoptions/)() | Предоставляет параметры, которые управляют нумерацией и расположением концевых сносок в этом разделе. |
| [get_FirstPageTray](./get_firstpagetray/)() | Получает лоток (контейнер) бумаги, используемый для первой страницы раздела. Значение зависит от реализации (принтера). |
| [get_FooterDistance](./get_footerdistance/)() | Возвращает или задает расстояние (в пунктах) между нижним колонтитулом и нижней границей страницы. |
| [get_FootnoteOptions](./get_footnoteoptions/)() | Предоставляет параметры, которые управляют нумерацией и расположением сносок в этом разделе. |
| [get_Gutter](./get_gutter/)() | Получает или задает количество дополнительного пространства, добавляемого к полю для переплёта документа. |
| [get_HeaderDistance](./get_headerdistance/)() | Возвращает или задает расстояние (в пунктах) между верхним колонтитулом и верхней границей страницы. |
| [get_HeadingLevelForChapter](./get_headinglevelforchapter/)() | Получает или задает стиль уровня заголовка, применяемый к названиям глав в документе. |
| [get_LayoutMode](./get_layoutmode/)() | Получает или задает режим макета этого раздела. |
| [get_LeftMargin](./get_leftmargin/)() | Возвращает или задает расстояние (в пунктах) между левым краем страницы и левой границей основного текста. |
| [get_LineNumberCountBy](./get_linenumbercountby/)() | Возвращает или задает числовой шаг для номеров строк. |
| [get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/)() | Получает или задает расстояние между правым краем номеров строк и левым краем документа. |
| [get_LineNumberRestartMode](./get_linenumberrestartmode/)() | Получает или задает способ нумерации строк, то есть начинается ли она заново в начале новой страницы или раздела, или продолжается непрерывно. |
| [get_LinesPerPage](./get_linesperpage/)() | Получает или задает количество строк на страницу в сетке документа. |
| [get_LineStartingNumber](./get_linestartingnumber/)() | Получает или задает начальный номер строки. |
| [get_Margins](./get_margins/)() | Возвращает или задает предустановленные [Margins](../margins/) страницы. |
| [get_MultiplePages](./get_multiplepages/)() const | Для многостраничных документов получает или задает способ печати или отображения документа, чтобы его можно было собрать в виде брошюры. |
| [get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/)() const | Истина, если документ имеет разные верхние и нижние колонтитулы для нечётных и чётных страниц. |
| [get_Orientation](./get_orientation/)() | Возвращает или задает ориентацию страницы. |
| [get_OtherPagesTray](./get_otherpagestray/)() | Получает лоток (контейнер) бумаги, используемый для всех страниц, кроме первой, раздела. Значение зависит от реализации (принтера). |
| [get_PageHeight](./get_pageheight/)() | Возвращает или задает высоту страницы в пунктах. |
| [get_PageNumberStyle](./get_pagenumberstyle/)() | Получает или задает формат номера страницы. |
| [get_PageStartingNumber](./get_pagestartingnumber/)() | Получает или задает начальный номер страницы раздела. |
| [get_PageWidth](./get_pagewidth/)() | Возвращает или задает ширину страницы в пунктах. |
| [get_PaperSize](./get_papersize/)() | Возвращает или задает размер бумаги. |
| [get_RestartPageNumbering](./get_restartpagenumbering/)() | True, если нумерация страниц начинается заново в начале раздела. |
| [get_RightMargin](./get_rightmargin/)() | Возвращает или задает расстояние (в пунктах) между правым краем страницы и правой границей основного текста. |
| [get_RtlGutter](./get_rtlgutter/)() | Получает или задает, использует ли Microsoft Word отступы (gutter) для раздела в зависимости от языка с направлением справа налево или слева направо. |
| [get_SectionStart](./get_sectionstart/)() | Возвращает или задает тип разрыва раздела для указанного объекта. |
| [get_SheetsPerBooklet](./get_sheetsperbooklet/)() const | Возвращает или задает количество страниц, включаемых в каждый буклет. |
| [get_SuppressEndnotes](./get_suppressendnotes/)() | True, если сноски печатаются в конце следующего раздела, который не подавляет сноски. Подавленные сноски печатаются перед сносками в этом разделе. |
| [get_TextColumns](./get_textcolumns/)() | Возвращает коллекцию, представляющую набор текстовых колонок. |
| [get_TextOrientation](./get_textorientation/)() | Позволяет указать [TextOrientation](./get_textorientation/) для всей страницы. Значение по умолчанию — [Horizontal](../textorientation/) |
| [get_TopMargin](./get_topmargin/)() | Возвращает или задает расстояние (в пунктах) между верхним краем страницы и верхней границей основного текста. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Возвращает или задает вертикальное выравнивание текста на каждой странице в документе или разделе. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bidi](./set_bidi/)(bool) | Сеттер для [Aspose::Words::PageSetup::get_Bidi](./get_bidi/). |
| [set_BorderAlwaysInFront](./set_borderalwaysinfront/)(bool) | Сеттер для [Aspose::Words::PageSetup::get_BorderAlwaysInFront](./get_borderalwaysinfront/). |
| [set_BorderAppliesTo](./set_borderappliesto/)(Aspose::Words::PageBorderAppliesTo) | Сеттер для [Aspose::Words::PageSetup::get_BorderAppliesTo](./get_borderappliesto/). |
| [set_BorderDistanceFrom](./set_borderdistancefrom/)(Aspose::Words::PageBorderDistanceFrom) | Сеттер для [Aspose::Words::PageSetup::get_BorderDistanceFrom](./get_borderdistancefrom/). |
| [set_BorderSurroundsFooter](./set_bordersurroundsfooter/)(bool) | Сеттер для [Aspose::Words::PageSetup::get_BorderSurroundsFooter](./get_bordersurroundsfooter/). |
| [set_BorderSurroundsHeader](./set_bordersurroundsheader/)(bool) | Сеттер для [Aspose::Words::PageSetup::get_BorderSurroundsHeader](./get_bordersurroundsheader/). |
| [set_BottomMargin](./set_bottommargin/)(double) | Сеттер для [Aspose::Words::PageSetup::get_BottomMargin](./get_bottommargin/). |
| [set_ChapterPageSeparator](./set_chapterpageseparator/)(Aspose::Words::ChapterPageSeparator) | Сеттер для [Aspose::Words::PageSetup::get_ChapterPageSeparator](./get_chapterpageseparator/). |
| [set_CharactersPerLine](./set_charactersperline/)(int32_t) | Сеттер для [Aspose::Words::PageSetup::get_CharactersPerLine](./get_charactersperline/). |
| [set_DifferentFirstPageHeaderFooter](./set_differentfirstpageheaderfooter/)(bool) | Сеттер для [Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/). |
| [set_FirstPageTray](./set_firstpagetray/)(int32_t) | Задает лоток (контейнер) бумаги, используемый для первой страницы раздела. Значение зависит от реализации (принтера). |
| [set_FooterDistance](./set_footerdistance/)(double) | Сеттер для [Aspose::Words::PageSetup::get_FooterDistance](./get_footerdistance/). |
| [set_Gutter](./set_gutter/)(double) | Сеттер для [Aspose::Words::PageSetup::get_Gutter](./get_gutter/). |
| [set_HeaderDistance](./set_headerdistance/)(double) | Сеттер для [Aspose::Words::PageSetup::get_HeaderDistance](./get_headerdistance/). |
| [set_HeadingLevelForChapter](./set_headinglevelforchapter/)(int32_t) | Сеттер для [Aspose::Words::PageSetup::get_HeadingLevelForChapter](./get_headinglevelforchapter/). |
| [set_LayoutMode](./set_layoutmode/)(Aspose::Words::SectionLayoutMode) | Сеттер для [Aspose::Words::PageSetup::get_LayoutMode](./get_layoutmode/). |
| [set_LeftMargin](./set_leftmargin/)(double) | Сеттер для [Aspose::Words::PageSetup::get_LeftMargin](./get_leftmargin/). |
| [set_LineNumberCountBy](./set_linenumbercountby/)(int32_t) | Сеттер для [Aspose::Words::PageSetup::get_LineNumberCountBy](./get_linenumbercountby/). |
| [set_LineNumberDistanceFromText](./set_linenumberdistancefromtext/)(double) | Сеттер для [Aspose::Words::PageSetup::get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/). |
| [set_LineNumberRestartMode](./set_linenumberrestartmode/)(Aspose::Words::LineNumberRestartMode) | Сеттер для [Aspose::Words::PageSetup::get_LineNumberRestartMode](./get_linenumberrestartmode/). |
| [set_LinesPerPage](./set_linesperpage/)(int32_t) | Сеттер для [Aspose::Words::PageSetup::get_LinesPerPage](./get_linesperpage/). |
| [set_LineStartingNumber](./set_linestartingnumber/)(int32_t) | Сеттер для [Aspose::Words::PageSetup::get_LineStartingNumber](./get_linestartingnumber/). |
| [set_Margins](./set_margins/)(Aspose::Words::Margins) | Сеттер для [Aspose::Words::PageSetup::get_Margins](./get_margins/). |
| [set_MultiplePages](./set_multiplepages/)(Aspose::Words::Settings::MultiplePagesType) | Сеттер для [Aspose::Words::PageSetup::get_MultiplePages](./get_multiplepages/). |
| [set_OddAndEvenPagesHeaderFooter](./set_oddandevenpagesheaderfooter/)(bool) | Сеттер для [Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Orientation) | Сеттер для [Aspose::Words::PageSetup::get_Orientation](./get_orientation/). |
| [set_OtherPagesTray](./set_otherpagestray/)(int32_t) | Устанавливает лоток (контейнер) бумаги, используемый для всех страниц раздела, кроме первой. Значение зависит от реализации (принтера). |
| [set_PageHeight](./set_pageheight/)(double) | Сеттер для [Aspose::Words::PageSetup::get_PageHeight](./get_pageheight/). |
| [set_PageNumberStyle](./set_pagenumberstyle/)(Aspose::Words::NumberStyle) | Сеттер для [Aspose::Words::PageSetup::get_PageNumberStyle](./get_pagenumberstyle/). |
| [set_PageStartingNumber](./set_pagestartingnumber/)(int32_t) | Сеттер для [Aspose::Words::PageSetup::get_PageStartingNumber](./get_pagestartingnumber/). |
| [set_PageWidth](./set_pagewidth/)(double) | Сеттер для [Aspose::Words::PageSetup::get_PageWidth](./get_pagewidth/). |
| [set_PaperSize](./set_papersize/)(Aspose::Words::PaperSize) | Сеттер для [Aspose::Words::PageSetup::get_PaperSize](./get_papersize/). |
| [set_RestartPageNumbering](./set_restartpagenumbering/)(bool) | Сеттер для [Aspose::Words::PageSetup::get_RestartPageNumbering](./get_restartpagenumbering/). |
| [set_RightMargin](./set_rightmargin/)(double) | Сеттер для [Aspose::Words::PageSetup::get_RightMargin](./get_rightmargin/). |
| [set_RtlGutter](./set_rtlgutter/)(bool) | Сеттер для [Aspose::Words::PageSetup::get_RtlGutter](./get_rtlgutter/). |
| [set_SectionStart](./set_sectionstart/)(Aspose::Words::SectionStart) | Сеттер для [Aspose::Words::PageSetup::get_SectionStart](./get_sectionstart/). |
| [set_SheetsPerBooklet](./set_sheetsperbooklet/)(int32_t) | Сеттер для [Aspose::Words::PageSetup::get_SheetsPerBooklet](./get_sheetsperbooklet/). |
| [set_SuppressEndnotes](./set_suppressendnotes/)(bool) | True, если сноски печатаются в конце следующего раздела, который не подавляет сноски. Подавленные сноски печатаются перед сносками в этом разделе. |
| [set_TextOrientation](./set_textorientation/)(Aspose::Words::TextOrientation) | Сеттер для [Aspose::Words::PageSetup::get_TextOrientation](./get_textorientation/). |
| [set_TopMargin](./set_topmargin/)(double) | Сеттер для [Aspose::Words::PageSetup::get_TopMargin](./get_topmargin/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::PageVerticalAlignment) | Сеттер для [Aspose::Words::PageSetup::get_VerticalAlignment](./get_verticalalignment/). |
| static [Type](./type/)() |  |
## Примечания


[PageSetup](./) object contains all the page setup attributes of a section (left margin, bottom margin, paper size, and so on) as properties.

## Примеры



Показывает, как применять и отменять настройки разметки страницы для разделов в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Измените свойства разметки страницы для текущего раздела построителя и добавьте текст.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// Если мы начнём новый раздел, используя построитель документа,
// он унаследует текущие свойства разметки страницы построителя.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// Мы можем вернуть его свойства разметки страницы к значениям по умолчанию, используя метод "ClearFormatting".
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

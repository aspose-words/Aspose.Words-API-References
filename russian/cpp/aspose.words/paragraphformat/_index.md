---
title: "класс Aspose::Words::ParagraphFormat"
linktitle: "ParagraphFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::ParagraphFormat. Представляет все форматирование абзаца. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 49000
url: /ru/cpp/aspose.words/paragraphformat/
---
## ParagraphFormat class


Представляет всё форматирование абзаца. Чтобы узнать больше, посетите статью документации [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class ParagraphFormat : public Aspose::Words::IBorderAttrSource,
                        public Aspose::Words::IShadingAttrSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Сбрасывает форматирование абзаца к значениям по умолчанию. |
| [get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/)() | Получает или задаёт флаг, указывающий, автоматически ли регулируется межсимвольный интервал между областями латинского текста и областями восточноазиатского текста в текущем абзаце. |
| [get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/)() | Получает или задаёт флаг, указывающий, автоматически ли регулируется межсимвольный интервал между областями цифр и областями восточноазиатского текста в текущем абзаце. |
| [get_Alignment](./get_alignment/)() | Получает или задает выравнивание текста для абзаца. |
| [get_BaselineAlignment](./get_baselinealignment/)() | Получает или задает вертикальное положение шрифтов в строке. |
| [get_Bidi](./get_bidi/)() | Получает или задает, является ли этот абзац направленным справа налево. |
| [get_Borders](./get_borders/)() | Получает коллекцию границ абзаца. |
| [get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/)() | Получает или задает значение (в символах) для первого абзацного отступа или висячего отступа. Используйте положительные значения для установки первого абзацного отступа и отрицательные значения для установки висячего отступа. |
| [get_CharacterUnitLeftIndent](./get_characterunitleftindent/)() | Получает или задает значение левого отступа (в символах) для указанных абзацев. |
| [get_CharacterUnitRightIndent](./get_characterunitrightindent/)() | Получает или задает значение правого отступа (в символах) для указанных абзацев. |
| [get_DropCapPosition](./get_dropcapposition/)() | Получает или задает позицию текста с броской буквой. |
| [get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/)() | Получает или задает флаг, указывающий, применяются ли правила разрыва строк для восточноазиатского текста к текущему абзацу. |
| [get_FirstLineIndent](./get_firstlineindent/)() | Получает или задает значение (в пунктах) для первого абзацного отступа или висячего отступа. Используйте положительные значения для установки первого абзацного отступа и отрицательные значения для установки висячего отступа. |
| [get_HangingPunctuation](./get_hangingpunctuation/)() | Получает или задает флаг, указывающий, включена ли висячая пунктуация для текущего абзаца. |
| [get_IsHeading](./get_isheading/)() | Истина, когда стиль абзаца является одним из встроенных стилей заголовков. |
| [get_IsListItem](./get_islistitem/)() | Истина, когда абзац является элементом маркированного или нумерованного списка. |
| [get_KeepTogether](./get_keeptogether/)() | Истина, если все строки в абзаце должны оставаться на одной странице. |
| [get_KeepWithNext](./get_keepwithnext/)() | Истина, если абзац должен оставаться на той же странице, что и следующий за ним абзац. |
| [get_LeftIndent](./get_leftindent/)() | Получает или задает значение (в пунктах), представляющее левый отступ для абзаца. |
| [get_LineSpacing](./get_linespacing/)() | Получает или задает межстрочный интервал (в пунктах) для абзаца. |
| [get_LineSpacingRule](./get_linespacingrule/)() | Получает или задает межстрочный интервал для абзаца. |
| [get_LinesToDrop](./get_linestodrop/)() | Получает или задает количество строк текста абзаца, используемых для расчёта высоты броской буквы. |
| [get_LineUnitAfter](./get_lineunitafter/)() | Получает или задает величину интервала (в сеточных линиях) после абзацев. |
| [get_LineUnitBefore](./get_lineunitbefore/)() | Получает или задает величину интервала (в сеточных линиях) перед абзацами. |
| [get_MirrorIndents](./get_mirrorindents/)() | Получает или задает флаг, указывающий, одинаковой ли ширины левый и правый отступы. |
| [get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/)() | Когда **true**, [SpaceBefore](./get_spacebefore/) и [SpaceAfter](./get_spaceafter/) будут игнорироваться между абзацами одного стиля. |
| [get_OutlineLevel](./get_outlinelevel/)() | Указывает уровень структуры абзаца в документе. |
| [get_PageBreakBefore](./get_pagebreakbefore/)() | Истина, если перед абзацем принудительно вставлен разрыв страницы. |
| [get_RightIndent](./get_rightindent/)() | Получает или задает значение (в пунктах), представляющее правый отступ абзаца. |
| [get_Shading](./get_shading/)() | Возвращает объект [Shading](../shading/), который относится к форматированию затенения абзаца. |
| [get_SnapToGrid](./get_snaptogrid/)() | Указывает, следует ли текущему абзацу использовать настройки линий сетки документа на страницу при размещении содержимого в абзаце. |
| [get_SpaceAfter](./get_spaceafter/)() | Получает или задает величину интервала (в пунктах) после абзаца. |
| [get_SpaceAfterAuto](./get_spaceafterauto/)() | True, если величина интервала после абзаца задается автоматически. |
| [get_SpaceBefore](./get_spacebefore/)() | Получает или задает величину интервала (в пунктах) перед абзацем. |
| [get_SpaceBeforeAuto](./get_spacebeforeauto/)() | True, если величина интервала перед абзацем задается автоматически. |
| [get_Style](./get_style/)() | Получает или задает стиль абзаца, применяемый к этому форматированию. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Получает или задает независимый от локали идентификатор стиля абзаца, применяемый к этому форматированию. |
| [get_StyleName](./get_stylename/)() | Получает или задает имя стиля абзаца, применяемого к этому форматированию. |
| [get_SuppressAutoHyphens](./get_suppressautohyphens/)() | Указывает, следует ли исключить текущий абзац из любой переноски слов, применяемой в настройках документа. |
| [get_SuppressLineNumbers](./get_suppresslinenumbers/)() | Указывает, следует ли исключить строки текущего абзаца из нумерации строк, применяемой в родительском разделе. |
| [get_TabStops](./get_tabstops/)() | Получает коллекцию пользовательских табуляций, определённых для этого объекта. |
| [get_WidowControl](./get_widowcontrol/)() | True, если первая и последняя строки абзаца должны оставаться на той же странице, что и остальная часть абзаца. |
| [get_WordWrap](./get_wordwrap/)() | Если это свойство имеет значение **false**, латинский текст в середине слова может переноситься в текущем абзаце. В противном случае латинский текст переносится целыми словами. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddSpaceBetweenFarEastAndAlpha](./set_addspacebetweenfareastandalpha/)(bool) | Сеттер для [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/). |
| [set_AddSpaceBetweenFarEastAndDigit](./set_addspacebetweenfareastanddigit/)(bool) | Сеттер для [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/). |
| [set_Alignment](./set_alignment/)(Aspose::Words::ParagraphAlignment) | Сеттер для [Aspose::Words::ParagraphFormat::get_Alignment](./get_alignment/). |
| [set_BaselineAlignment](./set_baselinealignment/)(Aspose::Words::BaselineAlignment) | Сеттер для [Aspose::Words::ParagraphFormat::get_BaselineAlignment](./get_baselinealignment/). |
| [set_Bidi](./set_bidi/)(bool) | Сеттер для [Aspose::Words::ParagraphFormat::get_Bidi](./get_bidi/). |
| [set_CharacterUnitFirstLineIndent](./set_characterunitfirstlineindent/)(double) | Сеттер для [Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/). |
| [set_CharacterUnitLeftIndent](./set_characterunitleftindent/)(double) | Сеттер для [Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent](./get_characterunitleftindent/). |
| [set_CharacterUnitRightIndent](./set_characterunitrightindent/)(double) | Сеттер для [Aspose::Words::ParagraphFormat::get_CharacterUnitRightIndent](./get_characterunitrightindent/). |
| [set_DropCapPosition](./set_dropcapposition/)(Aspose::Words::DropCapPosition) | Сеттер для [Aspose::Words::ParagraphFormat::get_DropCapPosition](./get_dropcapposition/). |
| [set_FarEastLineBreakControl](./set_fareastlinebreakcontrol/)(bool) | Сеттер для [Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/). |
| [set_FirstLineIndent](./set_firstlineindent/)(double) | Установщик для [Aspose::Words::ParagraphFormat::get_FirstLineIndent](./get_firstlineindent/). |
| [set_HangingPunctuation](./set_hangingpunctuation/)(bool) | Установщик для [Aspose::Words::ParagraphFormat::get_HangingPunctuation](./get_hangingpunctuation/). |
| [set_KeepTogether](./set_keeptogether/)(bool) | Установщик для [Aspose::Words::ParagraphFormat::get_KeepTogether](./get_keeptogether/). |
| [set_KeepWithNext](./set_keepwithnext/)(bool) | Установщик для [Aspose::Words::ParagraphFormat::get_KeepWithNext](./get_keepwithnext/). |
| [set_LeftIndent](./set_leftindent/)(double) | Установщик для [Aspose::Words::ParagraphFormat::get_LeftIndent](./get_leftindent/). |
| [set_LineSpacing](./set_linespacing/)(double) | Установщик для [Aspose::Words::ParagraphFormat::get_LineSpacing](./get_linespacing/). |
| [set_LineSpacingRule](./set_linespacingrule/)(Aspose::Words::LineSpacingRule) | Установщик для [Aspose::Words::ParagraphFormat::get_LineSpacingRule](./get_linespacingrule/). |
| [set_LinesToDrop](./set_linestodrop/)(int32_t) | Установщик для [Aspose::Words::ParagraphFormat::get_LinesToDrop](./get_linestodrop/). |
| [set_LineUnitAfter](./set_lineunitafter/)(double) | Установщик для [Aspose::Words::ParagraphFormat::get_LineUnitAfter](./get_lineunitafter/). |
| [set_LineUnitBefore](./set_lineunitbefore/)(double) | Установщик для [Aspose::Words::ParagraphFormat::get_LineUnitBefore](./get_lineunitbefore/). |
| [set_MirrorIndents](./set_mirrorindents/)(bool) | Установщик для [Aspose::Words::ParagraphFormat::get_MirrorIndents](./get_mirrorindents/). |
| [set_NoSpaceBetweenParagraphsOfSameStyle](./set_nospacebetweenparagraphsofsamestyle/)(bool) | Установщик для [Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/). |
| [set_OutlineLevel](./set_outlinelevel/)(Aspose::Words::OutlineLevel) | Установщик для [Aspose::Words::ParagraphFormat::get_OutlineLevel](./get_outlinelevel/). |
| [set_PageBreakBefore](./set_pagebreakbefore/)(bool) | Установщик для [Aspose::Words::ParagraphFormat::get_PageBreakBefore](./get_pagebreakbefore/). |
| [set_RightIndent](./set_rightindent/)(double) | Установщик для [Aspose::Words::ParagraphFormat::get_RightIndent](./get_rightindent/). |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | Установщик для [Aspose::Words::ParagraphFormat::get_SnapToGrid](./get_snaptogrid/). |
| [set_SpaceAfter](./set_spaceafter/)(double) | Установщик для [Aspose::Words::ParagraphFormat::get_SpaceAfter](./get_spaceafter/). |
| [set_SpaceAfterAuto](./set_spaceafterauto/)(bool) | Установщик для [Aspose::Words::ParagraphFormat::get_SpaceAfterAuto](./get_spaceafterauto/). |
| [set_SpaceBefore](./set_spacebefore/)(double) | Установщик для [Aspose::Words::ParagraphFormat::get_SpaceBefore](./get_spacebefore/). |
| [set_SpaceBeforeAuto](./set_spacebeforeauto/)(bool) | Установщик для [Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto](./get_spacebeforeauto/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Установщик для [Aspose::Words::ParagraphFormat::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Установщик для [Aspose::Words::ParagraphFormat::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Установщик для [Aspose::Words::ParagraphFormat::get_StyleName](./get_stylename/). |
| [set_SuppressAutoHyphens](./set_suppressautohyphens/)(bool) | Установщик для [Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens](./get_suppressautohyphens/). |
| [set_SuppressLineNumbers](./set_suppresslinenumbers/)(bool) | Установщик для [Aspose::Words::ParagraphFormat::get_SuppressLineNumbers](./get_suppresslinenumbers/). |
| [set_WidowControl](./set_widowcontrol/)(bool) | Сеттер для [Aspose::Words::ParagraphFormat::get_WidowControl](./get_widowcontrol/). |
| [set_WordWrap](./set_wordwrap/)(bool) | Сеттер для [Aspose::Words::ParagraphFormat::get_WordWrap](./get_wordwrap/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как вручную построить документ Aspose.Words.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Пустой документ содержит один раздел, одно тело и один абзац.
// Вызовите метод "RemoveAllChildren", чтобы удалить все эти узлы,
// и в результате получите узел документа без дочерних элементов.
doc->RemoveAllChildren();

// У этого документа теперь нет составных дочерних узлов, к которым мы могли бы добавить содержимое.
// Если мы захотим отредактировать его, нам потребуется заново заполнить его коллекцию узлов.
// Сначала создайте новый раздел, а затем добавьте его как дочерний элемент к корневому узлу документа.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Установите некоторые свойства разметки страницы для раздела.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Разделу требуется тело, которое будет содержать и отображать всё его содержимое
// на странице между заголовком и нижним колонтитулом раздела.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Создайте абзац, задайте некоторые свойства форматирования и затем добавьте его как дочерний элемент к телу.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Наконец, добавьте некоторое содержимое в документ. Создайте объект Run,
// задайте его внешний вид и содержимое, а затем добавьте его как дочерний элемент к абзацу.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

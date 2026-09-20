---
title: "Aspose::Words::Settings::Compatibility enum"
linktitle: "Compatibility"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::Compatibility enum. Указывает имена параметров совместимости в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.settings/compatibility/
---
## Compatibility enum


Указывает имена параметров совместимости.

```cpp
enum class Compatibility
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| NoTabHangInd | 0 | Нет отступа при висячей табуляции. |
| NoSpaceRaiseLower | 1 | Нет поднятия/опускания пробела. |
| SuppressSpBfAfterPgBrk | 2 | Подавлять пробел перед разрывом [Paragraph](../../aspose.words/paragraph/). |
| WrapTrailSpaces | 3 | Переносить завершающие пробелы. |
| PrintColBlack | 4 | Печать фона столбца. |
| NoColumnBalance | 5 | Без балансировки столбцов. |
| ConvMailMergeEsc | 6 | Преобразовать экранирование слияния почты. |
| SuppressTopSpacing | 7 | Подавлять верхний интервал. |
| UseSingleBorderforContiguousCells | 8 | Использовать одинарную [Border](../../aspose.words/border/) для смежных ячеек. |
| TransparentMetafiles | 9 | Прозрачные метафайлы. |
| ShowBreaksInFrames | 10 | Показывать разрывы в кадрах. |
| SwapBordersOddFacingPgs | 11 | Менять границы на нечётных страницах. |
| DoNotLeaveBackslashAlone | 12 | Не оставлять обратный слеш одиноким. |
| DoNotExpandOnShiftReturn | 13 | Не расширять при Shift+Return. |
| UlTrailSpace | 14 | Подчёркивать завершающий пробел. |
| BalanceSingleByteDoubleByteWidth | 15 | Уравнивать ширину однобайтовых и двубайтовых символов. |
| SuppressTopSpacingAtTopOfPage | 16 | Подавлять верхний интервал строк в WordPerfect. |
| SpacingInWholePoints | 17 | Интервал в целых пунктах. |
| PrintBodyTextBeforeHeader | 18 | Печатать текст [Body](../../aspose.words/body/) перед заголовком. |
| NoLeading | 19 | Без начального интервала. |
| SpaceForUL | 20 | Пространство для подчеркивания. |
| MWSmallCaps | 21 | MW Малые заглавные. |
| SuppressTopLineSpacingWP | 22 | Подавлять верхний интервал строк в WordPerfect. |
| TruncateFontHeightLikeWP6 | 23 | Обрезать высоту [Font](../../aspose.words/font/) как в WordPerfect 6. |
| SubFontBySize | 24 | Заменить [Font](../../aspose.words/font/) по размеру. |
| LineWrapLikeWord6 | 25 | Перенос строк как в Word 6. |
| DoNotSuppressParagraphBorder | 26 | Не подавлять [Paragraph](../../aspose.words/paragraph/)[Border](../../aspose.words/border/). |
| NoExtraLineSpacing | 27 | Без дополнительного межстрочного интервала. |
| SuppressBottomSpacing | 28 | Подавить нижний интервал. |
| WPSpaceWidth | 29 | Ширина пробела WordPerfect. |
| WPJustification | 30 | Выравнивание WordPerfect. |
| UsePrinterMetrics | 31 | Использовать метрики принтера. |
| ShapeLayoutLikeWW8 | 32 | Форма [Layout](../../aspose.words.layout/) как в Word 2000. |
| FootnoteLayoutLikeWW8 | 33 | Сноска [Layout](../../aspose.words.layout/) как в Word 2000. |
| DoNotUseHtmlParagraphAutoSpacing | 34 | Не использовать автоматический интервал HTML [Paragraph](../../aspose.words/paragraph/). |
| AdjustLineHeightInTable | 35 | Настроить высоту строки в таблице. |
| ForgetLastTabAlignment | 36 | Забыть выравнивание последней табуляции. |
| AutoSpaceLikeWord95 | 37 | Автоматический интервал как в Word 95. |
| AlignTableRowByRow | 38 | Выровнять строки таблицы по правилу. |
| LayoutRawTableWidth | 39 | [Layout](../../aspose.words.layout/) исходная ширина таблицы. |
| LayoutTableRowsApart | 40 | [Layout](../../aspose.words.layout/) строки таблицы раздельно. |
| UseWord97LineBreakRules | 41 | Использовать правила разрыва строк Word 97. |
| DoNotBreakWrappedTables | 42 | Не разрывать обернутые [Tables](../../aspose.words.tables/). |
| doNotSnapToGridInCell | 43 | Не привязывать к сетке в ячейках. |
| SelectFldWithFirstOrLastChar | 44 | Выбрать поле с первым или последним символом. |
| ApplyBreakingRules | 45 | Применить правила разрыва. |
| DoNotWrapTextWithPunct | 46 | Не переносить текст с пунктуацией. |
| DoNotUseEastAsianBreakRules | 47 | Не использовать правила разрыва восточноазиатского текста. |
| UseWord2002TableStyleRules | 48 | Использовать правила таблицы Word 2002 [Style](../../aspose.words/style/). |
| GrowAutofit | 49 | Увеличить автоподгонку. |
| UseNormalStyleForList | 50 | Использовать обычный [Style](../../aspose.words/style/) для списка. |
| DoNotUseIndentAsNumberingTabStop | 51 | Не использовать отступ как табуляцию нумерации. |
| UseAltKinsokuLineBreakRules | 52 | Использовать альтернативные правила разрыва линий Kinsoku. |
| AllowSpaceOfSameStyleInTable | 53 | Разрешить пространство одинакового [Style](../../aspose.words/style/) в таблице. |
| DoNotSuppressIndentation | 54 | Не подавлять отступ. |
| DoNotAutofitConstrainedTables | 55 | Не автоподгонять ограниченные [Tables](../../aspose.words.tables/). |
| AutofitToFirstFixedWidthCell | 56 | Автоподгонка к первой ячейке фиксированной ширины. |
| UnderlineTabInNumList | 57 | Подчеркнуть табуляцию в нумерованном списке. |
| DisplayHangulFixedWidth | 58 | Отображать Hangul фиксированной ширины. |
| SplitPgBreakAndParaMark | 59 | Разделить разрыв страницы и пометку [Paragraph](../../aspose.words/paragraph/). |
| DoNotVertAlignCellWithSp | 60 | Не выравнивать ячейку вертикально с интервалом. |
| DoNotBreakConstrainedForcedTable | 61 | Не разрывать ограниченные принудительные [Tables](../../aspose.words.tables/). |
| DoNotVertAlignInTxbx | 62 | Не выравнивать вертикально в текстовых полях. |
| UseAnsiKerningPairs | 63 | Использовать пары кернинга ANSI. |
| CachedColBalance | 64 | Кешированное балансирование столбцов. |
| UseFELayout | 65 | Использовать восточноазиатский [Layout](../../aspose.words.layout/). |
| UICompat97To2003 | 66 | Режим совместимости пользовательского интерфейса от Word 97 до Word 2003. |
| OverrideTableStyleFontSizeAndJustification | 67 | Переопределить размер и выравнивание [Style](../../aspose.words/style/)[Font](../../aspose.words/font/) таблицы. |
| DisableOpenTypeFontFormattingFeatures | 68 | Отключить функции форматирования OpenType [Font](../../aspose.words/font/). |
| SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning | 69 | Поменять местами внутри и снаружи для зеркальных отступов и относительного позиционирования. |
| UseWord2010TableStyleRules | 70 | Использовать правила [Style](../../aspose.words/style/) таблицы Word 2010. |

## См. также

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)

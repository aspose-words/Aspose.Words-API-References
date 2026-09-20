---
title: "Класс Aspose::Words::Settings::CompatibilityOptions"
linktitle: "CompatibilityOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Settings::CompatibilityOptions. Содержит параметры совместимости (то есть пользовательские настройки, введённые на вкладке Compatibility диалогового окна Options в Microsoft Word). Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.settings/compatibilityoptions/
---
## CompatibilityOptions class


Содержит параметры совместимости (то есть пользовательские настройки, введённые на вкладке **Compatibility** диалогового окна **Options** в Microsoft Word). Чтобы узнать больше, посетите статью документации [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/).

```cpp
class CompatibilityOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_AdjustLineHeightInTable](./get_adjustlineheightintable/)() | Добавить шаг сетки [Document](../../aspose.words/document/) к линиям в ячейках таблицы. |
| [get_AlignTablesRowByRow](./get_aligntablesrowbyrow/)() | Выравнивать строки таблицы независимо. |
| [get_AllowSpaceOfSameStyleInTable](./get_allowspaceofsamestyleintable/)() | Разрешить контекстуальный интервал абзацев в [Tables](../../aspose.words.tables/). |
| [get_ApplyBreakingRules](./get_applybreakingrules/)() | Использовать устаревшие правила разбиения строк для эфиопского и амхарского. |
| [get_AutofitToFirstFixedWidthCell](./get_autofittofirstfixedwidthcell/)() | Разрешить столбцам таблицы превышать предпочтительные ширины содержащихся ячеек. |
| [get_AutoSpaceLikeWord95](./get_autospacelikeword95/)() | Эмулировать полную ширину символов, как в Word 95. |
| [get_BalanceSingleByteDoubleByteWidth](./get_balancesinglebytedoublebytewidth/)() | Балансировать однобайтовые и двухбайтовые символы. |
| [get_CachedColBalance](./get_cachedcolbalance/)() | Использовать кэшированную информацию о [Paragraph](../../aspose.words/paragraph/) для балансировки столбцов. |
| [get_ConvMailMergeEsc](./get_convmailmergeesc/)() | Обрабатывать разделитель кавычек обратным слешем как две кавычки. |
| [get_DisableOpenTypeFontFormattingFeatures](./get_disableopentypefontformattingfeatures/)() | Указывает отключить функции форматирования шрифтов OpenType. |
| [get_DisplayHangulFixedWidth](./get_displayhangulfixedwidth/)() | Всегда использовать фиксированную ширину для символов Hangul. |
| [get_DoNotAutofitConstrainedTables](./get_donotautofitconstrainedtables/)() | Не автоматически подгонять [Tables](../../aspose.words.tables/) под размещение рядом с обтеканием объектов. |
| [get_DoNotBreakConstrainedForcedTable](./get_donotbreakconstrainedforcedtable/)() | Не разрывать строки таблицы вокруг плавающих [Tables](../../aspose.words.tables/). |
| [get_DoNotBreakWrappedTables](./get_donotbreakwrappedtables/)() | Не разрешать плавающим [Tables](../../aspose.words.tables/) разрываться через страницы. |
| [get_DoNotExpandShiftReturn](./get_donotexpandshiftreturn/)() | Не выравнивать строки, заканчивающиеся мягким разрывом строки. |
| [get_DoNotLeaveBackslashAlone](./get_donotleavebackslashalone/)() | Преобразовывать обратный слеш в знак йены при вводе. |
| [get_DoNotSnapToGridInCell](./get_donotsnaptogridincell/)() | Не привязываться к сетке [Document](../../aspose.words/document/) в ячейках таблицы с объектами. |
| [get_DoNotSuppressIndentation](./get_donotsuppressindentation/)() | Не игнорировать плавающие объекты при расчёте отступа [Paragraph](../../aspose.words/paragraph/). |
| [get_DoNotSuppressParagraphBorders](./get_donotsuppressparagraphborders/)() | Не подавлять границы [Paragraph](../../aspose.words/paragraph/) рядом с рамками. |
| [get_DoNotUseEastAsianBreakRules](./get_donotuseeastasianbreakrules/)() | Не сжимать сжимаемые символы при использовании сетки [Document](../../aspose.words/document/). |
| [get_DoNotUseHTMLParagraphAutoSpacing](./get_donotusehtmlparagraphautospacing/)() | Использовать фиксированный интервал [Paragraph](../../aspose.words/paragraph/) для автоматической настройки HTML. |
| [get_DoNotUseIndentAsNumberingTabStop](./get_donotuseindentasnumberingtabstop/)() | Игнорировать висячий отступ при создании табуляции после нумерации. |
| [get_DoNotVertAlignCellWithSp](./get_donotvertaligncellwithsp/)() | Не выравнивать ячейки, содержащие плавающие объекты, по вертикали. |
| [get_DoNotVertAlignInTxbx](./get_donotvertalignintxbx/)() | Игнорировать вертикальное выравнивание в текстовых полях. |
| [get_DoNotWrapTextWithPunct](./get_donotwraptextwithpunct/)() | Не разрешать висячую пунктуацию с сеткой символов. |
| [get_FootnoteLayoutLikeWW8](./get_footnotelayoutlikeww8/)() | Эмулировать размещение сносок Word 6.x/95/97. |
| [get_ForgetLastTabAlignment](./get_forgetlasttabalignment/)() | Игнорировать ширину последней табуляции при выравнивании [Paragraph](../../aspose.words/paragraph/), если он не выровнен по левому краю. |
| [get_GrowAutofit](./get_growautofit/)() | Разрешить [Tables](../../aspose.words.tables/) автоматически подгонять к полям страницы. |
| [get_LayoutRawTableWidth](./get_layoutrawtablewidth/)() | Игнорировать пробел перед таблицей при определении, должна ли таблица обтекать плавающий объект. |
| [get_LayoutTableRowsApart](./get_layouttablerowsapart/)() | Разрешить строкам таблицы независимо обтекать [Inline](../../aspose.words/inline/) объекты. |
| [get_LineWrapLikeWord6](./get_linewraplikeword6/)() | Эмулировать перенос строк Word 6.0 для восточноазиатского текста. |
| [get_MWSmallCaps](./get_mwsmallcaps/)() | Эмулировать Word 5.x для форматирования маленьких заглавных букв на Macintosh. |
| [get_NoColumnBalance](./get_nocolumnbalance/)() | Не выравнивать столбцы текста внутри [Section](../../aspose.words/section/). |
| [get_NoExtraLineSpacing](./get_noextralinespacing/)() | Не центрировать содержимое в строках с точной высотой строки. |
| [get_NoLeading](./get_noleading/)() | Не добавлять межстрочный интервал между строками текста. |
| [get_NoSpaceRaiseLower](./get_nospaceraiselower/)() | Не увеличивать высоту строки для поднятого/пониженного текста. |
| [get_NoTabHangInd](./get_notabhangind/)() | Не создавать пользовательскую табуляцию для висячего отступа. |
| [get_OverrideTableStyleFontSizeAndJustification](./get_overridetablestylefontsizeandjustification/)() | Указывает, как оценивается иерархия стилей документа. |
| [get_PrintBodyTextBeforeHeader](./get_printbodytextbeforeheader/)() | Печатать текст [Body](../../aspose.words/body/) перед содержимым верхнего/нижнего колонтитула. |
| [get_PrintColBlack](./get_printcolblack/)() | Печатать цвета в чёрно‑белом режиме без дизеринга. |
| [get_SelectFldWithFirstOrLastChar](./get_selectfldwithfirstorlastchar/)() | Выбирать поле, когда выбран первый или последний символ. |
| [get_ShapeLayoutLikeWW8](./get_shapelayoutlikeww8/)() | Эмулировать обтекание текста Word 97 вокруг плавающих объектов. |
| [get_ShowBreaksInFrames](./get_showbreaksinframes/)() | Отображать разрывы страниц/столбцов, присутствующие в рамках. |
| [get_SpaceForUL](./get_spaceforul/)() | Добавить дополнительное пространство ниже базовой линии для подчёркнутого восточноазиатского текста. |
| [get_SpacingInWholePoints](./get_spacinginwholepoints/)() | Только расширять/сжимать текст на целые пункты. |
| [get_SplitPgBreakAndParaMark](./get_splitpgbreakandparamark/)() | Всегда перемещать метку [Paragraph](../../aspose.words/paragraph/) на страницу после разрыва страницы. |
| [get_SubFontBySize](./get_subfontbysize/)() | Увеличить приоритет размера [Font](../../aspose.words/font/) при замене [Font](../../aspose.words/font/). |
| [get_SuppressBottomSpacing](./get_suppressbottomspacing/)() | Игнорировать точную высоту строки для последней строки на странице. |
| [get_SuppressSpacingAtTopOfPage](./get_suppressspacingattopofpage/)() | Игнорировать минимальную высоту строки для первой строки на странице. |
| [get_SuppressSpBfAfterPgBrk](./get_suppressspbfafterpgbrk/)() | Не использовать пробел перед первой строкой после разрыва страницы. |
| [get_SuppressTopSpacing](./get_suppresstopspacing/)() | Игнорировать минимальную и точную высоту строки для первой строки на странице. |
| [get_SuppressTopSpacingWP](./get_suppresstopspacingwp/)() | Эмулировать межстрочный интервал WordPerfect 5.x. |
| [get_SwapBordersFacingPgs](./get_swapbordersfacingpgs/)() | Менять границы [Paragraph](../../aspose.words/paragraph/) на нечётных страницах. |
| [get_SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning](./get_swapinsideandoutsideformirrorindentsandrelativepositioning/)() | Указывает менять внутреннюю и внешнюю стороны для зеркальных отступов и относительного позиционирования. |
| [get_TransparentMetafiles](./get_transparentmetafiles/)() | Указывает не очищать область за метафайловыми изображениями. |
| [get_TruncateFontHeightsLikeWP6](./get_truncatefontheightslikewp6/)() | Эмулировать расчёт высоты [Font](../../aspose.words/font/) в WordPerfect 6.x. |
| [get_UICompat97To2003](./get_uicompat97to2003/)() | True, чтобы отключить функции UI, несовместимые с Word97-2003. Значение по умолчанию — **false**. |
| [get_UlTrailSpace](./get_ultrailspace/)() | Подчёркивать все завершающие пробелы. |
| [get_UnderlineTabInNumList](./get_underlinetabinnumlist/)() | Подчёркивать следующий символ после нумерации. |
| [get_UseAltKinsokuLineBreakRules](./get_usealtkinsokulinebreakrules/)() | Использовать альтернативный набор правил переноса строк для восточноазиатского текста. |
| [get_UseAnsiKerningPairs](./get_useansikerningpairs/)() | Использовать пары кернинга ANSI из [Fonts](../../aspose.words.fonts/). |
| [get_UseFELayout](./get_usefelayout/)() | Не обходить код [Layout](../../aspose.words.layout/) для восточноазиатских/сложных скриптов. |
| [get_UseNormalStyleForList](./get_usenormalstyleforlist/)() | Не применять автоматически список [Paragraph](../../aspose.words/paragraph/)[Style](../../aspose.words/style/) к маркированному/нумерованному тексту. |
| [get_UsePrinterMetrics](./get_useprintermetrics/)() | Использовать метрики принтера для отображения документов. |
| [get_UseSingleBorderforContiguousCells](./get_usesingleborderforcontiguouscells/)() | Использовать упрощённые правила для конфликтов границ [Border](../../aspose.words/border/) таблиц. |
| [get_UseWord2002TableStyleRules](./get_useword2002tablestylerules/)() | Эмулировать правила [Style](../../aspose.words/style/) таблиц Word 2002. |
| [get_UseWord2010TableStyleRules](./get_useword2010tablestylerules/)() | Указывает использовать правила стилей таблиц Word2010. |
| [get_UseWord97LineBreakRules](./get_useword97linebreakrules/)() | Эмулировать перенос строк восточноазиатского текста Word 97. |
| [get_WPJustification](./get_wpjustification/)() | Эмулировать WordPerfect 6.x [Paragraph](../../aspose.words/paragraph/) выравнивание. |
| [get_WPSpaceWidth](./get_wpspacewidth/)() | Указывает, следует ли устанавливать ширину пробела так же, как в WordPerfect 5.x. |
| [get_WrapTrailSpaces](./get_wraptrailspaces/)() | Перенос строк с завершающими пробелами. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OptimizeFor](./optimizefor/)(Aspose::Words::Settings::MsWordVersion) | Позволяет оптимизировать содержимое документа, а также поведение по умолчанию Aspose.Words для определённых версий MS Word. Используйте этот метод, чтобы предотвратить отображение ленты "Compatibility mode" в MS Word при загрузке документа. (Обратите внимание, что также может потребоваться установить свойство [Compliance](../../aspose.words.saving/ooxmlsaveoptions/get_compliance/) в значение [Iso29500_2008_Transitional](../../aspose.words.saving/ooxmlcompliance/) или выше.) |
| [set_AdjustLineHeightInTable](./set_adjustlineheightintable/)(bool) | Добавить шаг сетки [Document](../../aspose.words/document/) к линиям в ячейках таблицы. |
| [set_AlignTablesRowByRow](./set_aligntablesrowbyrow/)(bool) | Выравнивать строки таблицы независимо. |
| [set_AllowSpaceOfSameStyleInTable](./set_allowspaceofsamestyleintable/)(bool) | Разрешить контекстуальный интервал абзацев в [Tables](../../aspose.words.tables/). |
| [set_ApplyBreakingRules](./set_applybreakingrules/)(bool) | Использовать устаревшие правила разбиения строк для эфиопского и амхарского. |
| [set_AutofitToFirstFixedWidthCell](./set_autofittofirstfixedwidthcell/)(bool) | Разрешить столбцам таблицы превышать предпочтительные ширины содержащихся ячеек. |
| [set_AutoSpaceLikeWord95](./set_autospacelikeword95/)(bool) | Эмулировать полную ширину символов, как в Word 95. |
| [set_BalanceSingleByteDoubleByteWidth](./set_balancesinglebytedoublebytewidth/)(bool) | Балансировать однобайтовые и двухбайтовые символы. |
| [set_CachedColBalance](./set_cachedcolbalance/)(bool) | Использовать кэшированную информацию о [Paragraph](../../aspose.words/paragraph/) для балансировки столбцов. |
| [set_ConvMailMergeEsc](./set_convmailmergeesc/)(bool) | Обрабатывать разделитель кавычек обратным слешем как две кавычки. |
| [set_DisableOpenTypeFontFormattingFeatures](./set_disableopentypefontformattingfeatures/)(bool) | Указывает отключить функции форматирования шрифтов OpenType. |
| [set_DisplayHangulFixedWidth](./set_displayhangulfixedwidth/)(bool) | Всегда использовать фиксированную ширину для символов Hangul. |
| [set_DoNotAutofitConstrainedTables](./set_donotautofitconstrainedtables/)(bool) | Не автоматически подгонять [Tables](../../aspose.words.tables/) под размещение рядом с обтеканием объектов. |
| [set_DoNotBreakConstrainedForcedTable](./set_donotbreakconstrainedforcedtable/)(bool) | Не разрывать строки таблицы вокруг плавающих [Tables](../../aspose.words.tables/). |
| [set_DoNotBreakWrappedTables](./set_donotbreakwrappedtables/)(bool) | Не разрешать плавающим [Tables](../../aspose.words.tables/) разрываться через страницы. |
| [set_DoNotExpandShiftReturn](./set_donotexpandshiftreturn/)(bool) | Не выравнивать строки, заканчивающиеся мягким разрывом строки. |
| [set_DoNotLeaveBackslashAlone](./set_donotleavebackslashalone/)(bool) | Преобразовывать обратный слеш в знак йены при вводе. |
| [set_DoNotSnapToGridInCell](./set_donotsnaptogridincell/)(bool) | Не привязываться к сетке [Document](../../aspose.words/document/) в ячейках таблицы с объектами. |
| [set_DoNotSuppressIndentation](./set_donotsuppressindentation/)(bool) | Не игнорировать плавающие объекты при расчёте отступа [Paragraph](../../aspose.words/paragraph/). |
| [set_DoNotSuppressParagraphBorders](./set_donotsuppressparagraphborders/)(bool) | Не подавлять границы [Paragraph](../../aspose.words/paragraph/) рядом с рамками. |
| [set_DoNotUseEastAsianBreakRules](./set_donotuseeastasianbreakrules/)(bool) | Не сжимать сжимаемые символы при использовании сетки [Document](../../aspose.words/document/). |
| [set_DoNotUseHTMLParagraphAutoSpacing](./set_donotusehtmlparagraphautospacing/)(bool) | Использовать фиксированный интервал [Paragraph](../../aspose.words/paragraph/) для автоматической настройки HTML. |
| [set_DoNotUseIndentAsNumberingTabStop](./set_donotuseindentasnumberingtabstop/)(bool) | Игнорировать висячий отступ при создании табуляции после нумерации. |
| [set_DoNotVertAlignCellWithSp](./set_donotvertaligncellwithsp/)(bool) | Не выравнивать ячейки, содержащие плавающие объекты, по вертикали. |
| [set_DoNotVertAlignInTxbx](./set_donotvertalignintxbx/)(bool) | Игнорировать вертикальное выравнивание в текстовых полях. |
| [set_DoNotWrapTextWithPunct](./set_donotwraptextwithpunct/)(bool) | Не разрешать висячую пунктуацию с сеткой символов. |
| [set_FootnoteLayoutLikeWW8](./set_footnotelayoutlikeww8/)(bool) | Эмулировать размещение сносок Word 6.x/95/97. |
| [set_ForgetLastTabAlignment](./set_forgetlasttabalignment/)(bool) | Игнорировать ширину последней табуляции при выравнивании [Paragraph](../../aspose.words/paragraph/), если он не выровнен по левому краю. |
| [set_GrowAutofit](./set_growautofit/)(bool) | Разрешить [Tables](../../aspose.words.tables/) автоматически подгонять к полям страницы. |
| [set_LayoutRawTableWidth](./set_layoutrawtablewidth/)(bool) | Игнорировать пробел перед таблицей при определении, должна ли таблица обтекать плавающий объект. |
| [set_LayoutTableRowsApart](./set_layouttablerowsapart/)(bool) | Разрешить строкам таблицы независимо обтекать [Inline](../../aspose.words/inline/) объекты. |
| [set_LineWrapLikeWord6](./set_linewraplikeword6/)(bool) | Эмулировать перенос строк Word 6.0 для восточноазиатского текста. |
| [set_MWSmallCaps](./set_mwsmallcaps/)(bool) | Эмулировать Word 5.x для форматирования маленьких заглавных букв на Macintosh. |
| [set_NoColumnBalance](./set_nocolumnbalance/)(bool) | Не выравнивать столбцы текста внутри [Section](../../aspose.words/section/). |
| [set_NoExtraLineSpacing](./set_noextralinespacing/)(bool) | Не центрировать содержимое в строках с точной высотой строки. |
| [set_NoLeading](./set_noleading/)(bool) | Не добавлять межстрочный интервал между строками текста. |
| [set_NoSpaceRaiseLower](./set_nospaceraiselower/)(bool) | Не увеличивать высоту строки для поднятого/пониженного текста. |
| [set_NoTabHangInd](./set_notabhangind/)(bool) | Не создавать пользовательскую табуляцию для висячего отступа. |
| [set_OverrideTableStyleFontSizeAndJustification](./set_overridetablestylefontsizeandjustification/)(bool) | Указывает, как оценивается иерархия стилей документа. |
| [set_PrintBodyTextBeforeHeader](./set_printbodytextbeforeheader/)(bool) | Печатать текст [Body](../../aspose.words/body/) перед содержимым верхнего/нижнего колонтитула. |
| [set_PrintColBlack](./set_printcolblack/)(bool) | Печатать цвета в чёрно‑белом режиме без дизеринга. |
| [set_SelectFldWithFirstOrLastChar](./set_selectfldwithfirstorlastchar/)(bool) | Выбирать поле, когда выбран первый или последний символ. |
| [set_ShapeLayoutLikeWW8](./set_shapelayoutlikeww8/)(bool) | Эмулировать обтекание текста Word 97 вокруг плавающих объектов. |
| [set_ShowBreaksInFrames](./set_showbreaksinframes/)(bool) | Отображать разрывы страниц/столбцов, присутствующие в рамках. |
| [set_SpaceForUL](./set_spaceforul/)(bool) | Добавить дополнительное пространство ниже базовой линии для подчёркнутого восточноазиатского текста. |
| [set_SpacingInWholePoints](./set_spacinginwholepoints/)(bool) | Только расширять/сжимать текст на целые пункты. |
| [set_SplitPgBreakAndParaMark](./set_splitpgbreakandparamark/)(bool) | Всегда перемещать метку [Paragraph](../../aspose.words/paragraph/) на страницу после разрыва страницы. |
| [set_SubFontBySize](./set_subfontbysize/)(bool) | Увеличить приоритет размера [Font](../../aspose.words/font/) при замене [Font](../../aspose.words/font/). |
| [set_SuppressBottomSpacing](./set_suppressbottomspacing/)(bool) | Игнорировать точную высоту строки для последней строки на странице. |
| [set_SuppressSpacingAtTopOfPage](./set_suppressspacingattopofpage/)(bool) | Игнорировать минимальную высоту строки для первой строки на странице. |
| [set_SuppressSpBfAfterPgBrk](./set_suppressspbfafterpgbrk/)(bool) | Не использовать пробел перед первой строкой после разрыва страницы. |
| [set_SuppressTopSpacing](./set_suppresstopspacing/)(bool) | Игнорировать минимальную и точную высоту строки для первой строки на странице. |
| [set_SuppressTopSpacingWP](./set_suppresstopspacingwp/)(bool) | Эмулировать межстрочный интервал WordPerfect 5.x. |
| [set_SwapBordersFacingPgs](./set_swapbordersfacingpgs/)(bool) | Менять границы [Paragraph](../../aspose.words/paragraph/) на нечётных страницах. |
| [set_SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning](./set_swapinsideandoutsideformirrorindentsandrelativepositioning/)(bool) | Указывает менять внутреннюю и внешнюю стороны для зеркальных отступов и относительного позиционирования. |
| [set_TransparentMetafiles](./set_transparentmetafiles/)(bool) | Указывает не очищать область за метафайловыми изображениями. |
| [set_TruncateFontHeightsLikeWP6](./set_truncatefontheightslikewp6/)(bool) | Эмулировать расчёт высоты [Font](../../aspose.words/font/) в WordPerfect 6.x. |
| [set_UICompat97To2003](./set_uicompat97to2003/)(bool) | True, чтобы отключить функции UI, несовместимые с Word97-2003. Значение по умолчанию — **false**. |
| [set_UlTrailSpace](./set_ultrailspace/)(bool) | Подчёркивать все завершающие пробелы. |
| [set_UnderlineTabInNumList](./set_underlinetabinnumlist/)(bool) | Подчёркивать следующий символ после нумерации. |
| [set_UseAltKinsokuLineBreakRules](./set_usealtkinsokulinebreakrules/)(bool) | Использовать альтернативный набор правил переноса строк для восточноазиатского текста. |
| [set_UseAnsiKerningPairs](./set_useansikerningpairs/)(bool) | Использовать пары кернинга ANSI из [Fonts](../../aspose.words.fonts/). |
| [set_UseFELayout](./set_usefelayout/)(bool) | Не обходить код [Layout](../../aspose.words.layout/) для восточноазиатских/сложных скриптов. |
| [set_UseNormalStyleForList](./set_usenormalstyleforlist/)(bool) | Не применять автоматически список [Paragraph](../../aspose.words/paragraph/)[Style](../../aspose.words/style/) к маркированному/нумерованному тексту. |
| [set_UsePrinterMetrics](./set_useprintermetrics/)(bool) | Использовать метрики принтера для отображения документов. |
| [set_UseSingleBorderforContiguousCells](./set_usesingleborderforcontiguouscells/)(bool) | Использовать упрощённые правила для конфликтов границ [Border](../../aspose.words/border/) таблиц. |
| [set_UseWord2002TableStyleRules](./set_useword2002tablestylerules/)(bool) | Эмулировать правила [Style](../../aspose.words/style/) таблиц Word 2002. |
| [set_UseWord2010TableStyleRules](./set_useword2010tablestylerules/)(bool) | Указывает использовать правила стилей таблиц Word2010. |
| [set_UseWord97LineBreakRules](./set_useword97linebreakrules/)(bool) | Эмулировать перенос строк восточноазиатского текста Word 97. |
| [set_WPJustification](./set_wpjustification/)(bool) | Эмулировать WordPerfect 6.x [Paragraph](../../aspose.words/paragraph/) выравнивание. |
| [set_WPSpaceWidth](./set_wpspacewidth/)(bool) | Указывает, следует ли устанавливать ширину пробела так же, как в WordPerfect 5.x. |
| [set_WrapTrailSpaces](./set_wraptrailspaces/)(bool) | Перенос строк с завершающими пробелами. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как задать спецификацию соответствия OOXML для сохраняемого документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Если мы настроим параметры совместимости для соответствия Microsoft Word 2003,
// вставка изображения определит его форму с использованием VML.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Vml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());

// Стандарт OOXML "ISO/IEC 29500:2008" не поддерживает формы VML.
// Если мы установим свойство "Compliance" объекта SaveOptions в значение "OoxmlCompliance.Iso29500_2008_Strict",
// любой документ, сохраняемый с этим объектом, должен будет соответствовать этому стандарту.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docx);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Наш сохраняемый документ определяет форму с использованием DML, чтобы соответствовать стандарту OOXML "ISO/IEC 29500:2008".
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());
```


Показывает, как вертикально выровнять текстовое содержимое текстового поля.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// Установите свойство "VerticalAnchor" в значение "TextBoxAnchor.Top", чтобы
// выравнять текст в этом текстовом поле по верхней стороне фигуры.
// Установите свойство "VerticalAnchor" в значение "TextBoxAnchor.Middle", чтобы
// выравнять текст в этом текстовом поле по центру фигуры.
// Установите свойство "VerticalAnchor" в значение "TextBoxAnchor.Bottom", чтобы
// выравнять текст в этом текстовом поле по нижней части фигуры.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// Вертикальное выравнивание текста внутри текстовых полей доступно, начиная с Microsoft Word 2007.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## См. также

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)

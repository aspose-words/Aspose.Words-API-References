---
title: CompatibilityOptions
second_title: Справочник по API Aspose.Words для Java
description: Содержит параметры совместимости, которые представляют собой пользовательские настройки, введенные на вкладке «Совместимость» диалогового окна «Параметры» в Microsoft Word.
type: docs
weight: 86
url: /ru/java/com.aspose.words/compatibilityoptions/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class CompatibilityOptions implements Cloneable
```

 Содержит параметры совместимости (то есть пользовательские настройки, введенные на**Compatibility** вкладка**Options** диалоговое окно в Microsoft Word).

 Чтобы узнать больше, посетите**Detect File Format and Check Format Compatibility** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAdjustLineHeightInTable()](#getAdjustLineHeightInTable--) | Добавьте шаг линии сетки документа к строкам в ячейках таблицы. |
| [getAlignTablesRowByRow()](#getAlignTablesRowByRow--) | Выравнивание строк таблицы независимо. |
| [getAllowSpaceOfSameStyleInTable()](#getAllowSpaceOfSameStyleInTable--) | Разрешить контекстное расстояние между абзацами в таблицах. |
| [getApplyBreakingRules()](#getApplyBreakingRules--) | Используйте устаревшие правила разбиения строк на эфиопском и амхарском языках. |
| [getAutoSpaceLikeWord95()](#getAutoSpaceLikeWord95--) | Эмуляция полноширинного межсимвольного интервала Word 95. |
| [getAutofitToFirstFixedWidthCell()](#getAutofitToFirstFixedWidthCell--) | Разрешить столбцам таблицы превышать предпочтительную ширину составляющих ячеек. |
| [getBalanceSingleByteDoubleByteWidth()](#getBalanceSingleByteDoubleByteWidth--) | Сбалансируйте однобайтовые и двухбайтовые символы. |
| [getCachedColBalance()](#getCachedColBalance--) | Используйте кэшированную информацию об абзацах для балансировки столбцов. |
| [getClass()](#getClass--) |  |
| [getConvMailMergeEsc()](#getConvMailMergeEsc--) | Рассматривайте разделитель кавычек с обратной косой чертой как две кавычки. |
| [getDisableOpenTypeFontFormattingFeatures()](#getDisableOpenTypeFontFormattingFeatures--) |  |
| [getDisplayHangulFixedWidth()](#getDisplayHangulFixedWidth--) | Всегда используйте фиксированную ширину для символов хангыль. |
| [getDoNotAutofitConstrainedTables()](#getDoNotAutofitConstrainedTables--) | Не используйте автоподгонку таблиц для размещения рядом с обернутыми объектами. |
| [getDoNotBreakConstrainedForcedTable()](#getDoNotBreakConstrainedForcedTable--) | Не разбивайте строки таблицы вокруг плавающих таблиц. |
| [getDoNotBreakWrappedTables()](#getDoNotBreakWrappedTables--) | Не позволяйте плавающим таблицам разбиваться на страницы. |
| [getDoNotExpandShiftReturn()](#getDoNotExpandShiftReturn--) | Не выравнивайте строки, заканчивающиеся мягким разрывом строки. |
| [getDoNotLeaveBackslashAlone()](#getDoNotLeaveBackslashAlone--) | Преобразование обратной косой черты в знак иены при вводе. |
| [getDoNotSnapToGridInCell()](#getDoNotSnapToGridInCell--) | Не привязываться к сетке документа в ячейках таблицы с объектами. |
| [getDoNotSuppressIndentation()](#getDoNotSuppressIndentation--) | Не игнорируйте плавающие объекты при расчете отступа абзаца. |
| [getDoNotSuppressParagraphBorders()](#getDoNotSuppressParagraphBorders--) | Не подавлять границы абзаца рядом с фреймами. |
| [getDoNotUseEastAsianBreakRules()](#getDoNotUseEastAsianBreakRules--) | Не сжимайте сжимаемые символы при использовании сетки документа. |
| [getDoNotUseHTMLParagraphAutoSpacing()](#getDoNotUseHTMLParagraphAutoSpacing--) | Используйте фиксированный интервал между абзацами для автоматической настройки HTML. |
| [getDoNotUseIndentAsNumberingTabStop()](#getDoNotUseIndentAsNumberingTabStop--) | Игнорировать висячий отступ при создании позиции табуляции после нумерации. |
| [getDoNotVertAlignCellWithSp()](#getDoNotVertAlignCellWithSp--) | Не выравнивайте по вертикали ячейки, содержащие плавающие объекты. |
| [getDoNotVertAlignInTxbx()](#getDoNotVertAlignInTxbx--) | Игнорировать вертикальное выравнивание в текстовых полях. |
| [getDoNotWrapTextWithPunct()](#getDoNotWrapTextWithPunct--) | Не разрешать висячие знаки препинания с сеткой символов. |
| [getFootnoteLayoutLikeWW8()](#getFootnoteLayoutLikeWW8--) | Эмулировать размещение сносок Word 6.x/95/97. |
| [getForgetLastTabAlignment()](#getForgetLastTabAlignment--) | Игнорировать ширину последней позиции табуляции при выравнивании абзаца, если он не выровнен по левому краю. |
| [getGrowAutofit()](#getGrowAutofit--) | Разрешить автоподгонку таблиц к полям страницы. |
| [getLayoutRawTableWidth()](#getLayoutRawTableWidth--) | Игнорировать пробел перед таблицей при принятии решения о том, должна ли таблица оборачивать плавающий объект. |
| [getLayoutTableRowsApart()](#getLayoutTableRowsApart--) | Разрешить строкам таблицы независимо оборачивать встроенные объекты. |
| [getLineWrapLikeWord6()](#getLineWrapLikeWord6--) | Эмуляция переноса строк Word 6.0 для восточноазиатского текста. |
| [getMWSmallCaps()](#getMWSmallCaps--) | Эмулируйте Word 5.x для форматирования малых заглавных букв в Macintosh. |
| [getNoColumnBalance()](#getNoColumnBalance--) | Не балансируйте текстовые столбцы в разделе. |
| [getNoExtraLineSpacing()](#getNoExtraLineSpacing--) | Не центрируйте содержимое на строках с точной высотой строки. |
| [getNoLeading()](#getNoLeading--) | Не добавляйте интерлиньяж между строками текста. |
| [getNoSpaceRaiseLower()](#getNoSpaceRaiseLower--) | Не увеличивать высоту строки для приподнятого/пониженного текста. |
| [getNoTabHangInd()](#getNoTabHangInd--) | Не создавайте пользовательскую позицию табуляции для висячего отступа. |
| [getOverrideTableStyleFontSizeAndJustification()](#getOverrideTableStyleFontSizeAndJustification--) | Указывает, как оценивается иерархия стилей документа. |
| [getPrintBodyTextBeforeHeader()](#getPrintBodyTextBeforeHeader--) | Печатать основной текст перед содержимым верхнего/нижнего колонтитула. |
| [getPrintColBlack()](#getPrintColBlack--) | Печатайте цвета как черно-белые без дизеринга. |
| [getSelectFldWithFirstOrLastChar()](#getSelectFldWithFirstOrLastChar--) | Выберите поле, когда выбран первый или последний символ. |
| [getShapeLayoutLikeWW8()](#getShapeLayoutLikeWW8--) | Эмуляция переноса текста Word 97 вокруг плавающих объектов. |
| [getShowBreaksInFrames()](#getShowBreaksInFrames--) | Отображение разрывов страниц/столбцов во фреймах. |
| [getSpaceForUL()](#getSpaceForUL--) | Добавьте дополнительное пространство ниже базовой линии для подчеркнутого восточноазиатского текста. |
| [getSpacingInWholePoints()](#getSpacingInWholePoints--) | Расширить/сжать текст только по целым точкам. |
| [getSplitPgBreakAndParaMark()](#getSplitPgBreakAndParaMark--) | Всегда перемещайте метку абзаца на страницу после разрыва страницы. |
| [getSubFontBySize()](#getSubFontBySize--) | Увеличьте приоритет размера шрифта при замене шрифта. |
| [getSuppressBottomSpacing()](#getSuppressBottomSpacing--) | Игнорировать точную высоту строки для последней строки на странице. |
| [getSuppressSpBfAfterPgBrk()](#getSuppressSpBfAfterPgBrk--) | Не используйте пробел перед первой строкой после разрыва страницы. |
| [getSuppressSpacingAtTopOfPage()](#getSuppressSpacingAtTopOfPage--) | Игнорировать минимальную высоту строки для первой строки на странице. |
| [getSuppressTopSpacing()](#getSuppressTopSpacing--) | Игнорировать минимальную и точную высоту строки для первой строки на странице. |
| [getSuppressTopSpacingWP()](#getSuppressTopSpacingWP--) | Эмуляция межстрочного интервала WordPerfect 5.x. |
| [getSwapBordersFacingPgs()](#getSwapBordersFacingPgs--) | Поменять местами границы абзаца на страницах с нечетными номерами. |
| [getSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning()](#getSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning--) |  |
| [getTransparentMetafiles()](#getTransparentMetafiles--) | Указывает, что область за изображениями метафайла не очищается. |
| [getTruncateFontHeightsLikeWP6()](#getTruncateFontHeightsLikeWP6--) | Эмуляция вычисления высоты шрифта WordPerfect 6.x. |
| [getUICompat97To2003()](#getUICompat97To2003--) | **True** чтобы отключить функциональность пользовательского интерфейса, несовместимую с Word97-2003. |
| [getUlTrailSpace()](#getUlTrailSpace--) | Подчеркните все конечные пробелы. |
| [getUnderlineTabInNumList()](#getUnderlineTabInNumList--) | Подчеркните следующий символ после нумерации. |
| [getUseAltKinsokuLineBreakRules()](#getUseAltKinsokuLineBreakRules--) | Используйте альтернативный набор восточноазиатских правил разрыва линии. |
| [getUseAnsiKerningPairs()](#getUseAnsiKerningPairs--) | Используйте пары кернинга ANSI из шрифтов. |
| [getUseFELayout()](#getUseFELayout--) | Не обходите восточноазиатский/сложный код макета сценария. |
| [getUseNormalStyleForList()](#getUseNormalStyleForList--) | Не применять автоматически стиль абзаца списка к маркированному/нумерованному тексту. |
| [getUsePrinterMetrics()](#getUsePrinterMetrics--) | Используйте показатели принтера для отображения документов. |
| [getUseSingleBorderforContiguousCells()](#getUseSingleBorderforContiguousCells--) | Используйте упрощенные правила для конфликтов границ таблицы. |
| [getUseWord2002TableStyleRules()](#getUseWord2002TableStyleRules--) | Эмулировать правила стиля таблицы Word 2002. |
| [getUseWord2010TableStyleRules()](#getUseWord2010TableStyleRules--) |  |
| [getUseWord97LineBreakRules()](#getUseWord97LineBreakRules--) | Эмуляция разрыва строки Word 97 в Восточной Азии. |
| [getWPJustification()](#getWPJustification--) | Эмуляция выравнивания абзаца WordPerfect 6.x. |
| [getWPSpaceWidth()](#getWPSpaceWidth--) | Указывает, следует ли устанавливать ширину пробела, как это делается в WordPerfect 5.x. |
| [getWrapTrailSpaces()](#getWrapTrailSpaces--) | Завершающие пробелы переноса строк. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [optimizeFor(int version)](#optimizeFor-int-) |  |
| [setAdjustLineHeightInTable(boolean value)](#setAdjustLineHeightInTable-boolean-) | Добавьте шаг линии сетки документа к строкам в ячейках таблицы. |
| [setAlignTablesRowByRow(boolean value)](#setAlignTablesRowByRow-boolean-) | Выравнивание строк таблицы независимо. |
| [setAllowSpaceOfSameStyleInTable(boolean value)](#setAllowSpaceOfSameStyleInTable-boolean-) | Разрешить контекстное расстояние между абзацами в таблицах. |
| [setApplyBreakingRules(boolean value)](#setApplyBreakingRules-boolean-) | Используйте устаревшие правила разбиения строк на эфиопском и амхарском языках. |
| [setAutoSpaceLikeWord95(boolean value)](#setAutoSpaceLikeWord95-boolean-) | Эмуляция полноширинного межсимвольного интервала Word 95. |
| [setAutofitToFirstFixedWidthCell(boolean value)](#setAutofitToFirstFixedWidthCell-boolean-) | Разрешить столбцам таблицы превышать предпочтительную ширину составляющих ячеек. |
| [setBalanceSingleByteDoubleByteWidth(boolean value)](#setBalanceSingleByteDoubleByteWidth-boolean-) | Сбалансируйте однобайтовые и двухбайтовые символы. |
| [setCachedColBalance(boolean value)](#setCachedColBalance-boolean-) | Используйте кэшированную информацию об абзацах для балансировки столбцов. |
| [setConvMailMergeEsc(boolean value)](#setConvMailMergeEsc-boolean-) | Рассматривайте разделитель кавычек с обратной косой чертой как две кавычки. |
| [setDisableOpenTypeFontFormattingFeatures(boolean value)](#setDisableOpenTypeFontFormattingFeatures-boolean-) |  |
| [setDisplayHangulFixedWidth(boolean value)](#setDisplayHangulFixedWidth-boolean-) | Всегда используйте фиксированную ширину для символов хангыль. |
| [setDoNotAutofitConstrainedTables(boolean value)](#setDoNotAutofitConstrainedTables-boolean-) | Не используйте автоподгонку таблиц для размещения рядом с обернутыми объектами. |
| [setDoNotBreakConstrainedForcedTable(boolean value)](#setDoNotBreakConstrainedForcedTable-boolean-) | Не разбивайте строки таблицы вокруг плавающих таблиц. |
| [setDoNotBreakWrappedTables(boolean value)](#setDoNotBreakWrappedTables-boolean-) | Не позволяйте плавающим таблицам разбиваться на страницы. |
| [setDoNotExpandShiftReturn(boolean value)](#setDoNotExpandShiftReturn-boolean-) | Не выравнивайте строки, заканчивающиеся мягким разрывом строки. |
| [setDoNotLeaveBackslashAlone(boolean value)](#setDoNotLeaveBackslashAlone-boolean-) | Преобразование обратной косой черты в знак иены при вводе. |
| [setDoNotSnapToGridInCell(boolean value)](#setDoNotSnapToGridInCell-boolean-) | Не привязываться к сетке документа в ячейках таблицы с объектами. |
| [setDoNotSuppressIndentation(boolean value)](#setDoNotSuppressIndentation-boolean-) | Не игнорируйте плавающие объекты при расчете отступа абзаца. |
| [setDoNotSuppressParagraphBorders(boolean value)](#setDoNotSuppressParagraphBorders-boolean-) | Не подавлять границы абзаца рядом с фреймами. |
| [setDoNotUseEastAsianBreakRules(boolean value)](#setDoNotUseEastAsianBreakRules-boolean-) | Не сжимайте сжимаемые символы при использовании сетки документа. |
| [setDoNotUseHTMLParagraphAutoSpacing(boolean value)](#setDoNotUseHTMLParagraphAutoSpacing-boolean-) | Используйте фиксированный интервал между абзацами для автоматической настройки HTML. |
| [setDoNotUseIndentAsNumberingTabStop(boolean value)](#setDoNotUseIndentAsNumberingTabStop-boolean-) | Игнорировать висячий отступ при создании позиции табуляции после нумерации. |
| [setDoNotVertAlignCellWithSp(boolean value)](#setDoNotVertAlignCellWithSp-boolean-) | Не выравнивайте по вертикали ячейки, содержащие плавающие объекты. |
| [setDoNotVertAlignInTxbx(boolean value)](#setDoNotVertAlignInTxbx-boolean-) | Игнорировать вертикальное выравнивание в текстовых полях. |
| [setDoNotWrapTextWithPunct(boolean value)](#setDoNotWrapTextWithPunct-boolean-) | Не разрешать висячие знаки препинания с сеткой символов. |
| [setFootnoteLayoutLikeWW8(boolean value)](#setFootnoteLayoutLikeWW8-boolean-) | Эмулировать размещение сносок Word 6.x/95/97. |
| [setForgetLastTabAlignment(boolean value)](#setForgetLastTabAlignment-boolean-) | Игнорировать ширину последней позиции табуляции при выравнивании абзаца, если он не выровнен по левому краю. |
| [setGrowAutofit(boolean value)](#setGrowAutofit-boolean-) | Разрешить автоподгонку таблиц к полям страницы. |
| [setLayoutRawTableWidth(boolean value)](#setLayoutRawTableWidth-boolean-) | Игнорировать пробел перед таблицей при принятии решения о том, должна ли таблица оборачивать плавающий объект. |
| [setLayoutTableRowsApart(boolean value)](#setLayoutTableRowsApart-boolean-) | Разрешить строкам таблицы независимо оборачивать встроенные объекты. |
| [setLineWrapLikeWord6(boolean value)](#setLineWrapLikeWord6-boolean-) | Эмуляция переноса строк Word 6.0 для восточноазиатского текста. |
| [setMWSmallCaps(boolean value)](#setMWSmallCaps-boolean-) | Эмулируйте Word 5.x для форматирования малых заглавных букв в Macintosh. |
| [setNoColumnBalance(boolean value)](#setNoColumnBalance-boolean-) | Не балансируйте текстовые столбцы в разделе. |
| [setNoExtraLineSpacing(boolean value)](#setNoExtraLineSpacing-boolean-) | Не центрируйте содержимое на строках с точной высотой строки. |
| [setNoLeading(boolean value)](#setNoLeading-boolean-) | Не добавляйте интерлиньяж между строками текста. |
| [setNoSpaceRaiseLower(boolean value)](#setNoSpaceRaiseLower-boolean-) | Не увеличивать высоту строки для приподнятого/пониженного текста. |
| [setNoTabHangInd(boolean value)](#setNoTabHangInd-boolean-) | Не создавайте пользовательскую позицию табуляции для висячего отступа. |
| [setOverrideTableStyleFontSizeAndJustification(boolean value)](#setOverrideTableStyleFontSizeAndJustification-boolean-) | Указывает, как оценивается иерархия стилей документа. |
| [setPrintBodyTextBeforeHeader(boolean value)](#setPrintBodyTextBeforeHeader-boolean-) | Печатать основной текст перед содержимым верхнего/нижнего колонтитула. |
| [setPrintColBlack(boolean value)](#setPrintColBlack-boolean-) | Печатайте цвета как черно-белые без дизеринга. |
| [setSelectFldWithFirstOrLastChar(boolean value)](#setSelectFldWithFirstOrLastChar-boolean-) | Выберите поле, когда выбран первый или последний символ. |
| [setShapeLayoutLikeWW8(boolean value)](#setShapeLayoutLikeWW8-boolean-) | Эмуляция переноса текста Word 97 вокруг плавающих объектов. |
| [setShowBreaksInFrames(boolean value)](#setShowBreaksInFrames-boolean-) | Отображение разрывов страниц/столбцов во фреймах. |
| [setSpaceForUL(boolean value)](#setSpaceForUL-boolean-) | Добавьте дополнительное пространство ниже базовой линии для подчеркнутого восточноазиатского текста. |
| [setSpacingInWholePoints(boolean value)](#setSpacingInWholePoints-boolean-) | Расширить/сжать текст только по целым точкам. |
| [setSplitPgBreakAndParaMark(boolean value)](#setSplitPgBreakAndParaMark-boolean-) | Всегда перемещайте метку абзаца на страницу после разрыва страницы. |
| [setSubFontBySize(boolean value)](#setSubFontBySize-boolean-) | Увеличьте приоритет размера шрифта при замене шрифта. |
| [setSuppressBottomSpacing(boolean value)](#setSuppressBottomSpacing-boolean-) | Игнорировать точную высоту строки для последней строки на странице. |
| [setSuppressSpBfAfterPgBrk(boolean value)](#setSuppressSpBfAfterPgBrk-boolean-) | Не используйте пробел перед первой строкой после разрыва страницы. |
| [setSuppressSpacingAtTopOfPage(boolean value)](#setSuppressSpacingAtTopOfPage-boolean-) | Игнорировать минимальную высоту строки для первой строки на странице. |
| [setSuppressTopSpacing(boolean value)](#setSuppressTopSpacing-boolean-) | Игнорировать минимальную и точную высоту строки для первой строки на странице. |
| [setSuppressTopSpacingWP(boolean value)](#setSuppressTopSpacingWP-boolean-) | Эмуляция межстрочного интервала WordPerfect 5.x. |
| [setSwapBordersFacingPgs(boolean value)](#setSwapBordersFacingPgs-boolean-) | Поменять местами границы абзаца на страницах с нечетными номерами. |
| [setSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning(boolean value)](#setSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning-boolean-) |  |
| [setTransparentMetafiles(boolean value)](#setTransparentMetafiles-boolean-) | Указывает, что область за изображениями метафайла не очищается. |
| [setTruncateFontHeightsLikeWP6(boolean value)](#setTruncateFontHeightsLikeWP6-boolean-) | Эмуляция вычисления высоты шрифта WordPerfect 6.x. |
| [setUICompat97To2003(boolean value)](#setUICompat97To2003-boolean-) | **True** чтобы отключить функциональность пользовательского интерфейса, несовместимую с Word97-2003. |
| [setUlTrailSpace(boolean value)](#setUlTrailSpace-boolean-) | Подчеркните все конечные пробелы. |
| [setUnderlineTabInNumList(boolean value)](#setUnderlineTabInNumList-boolean-) | Подчеркните следующий символ после нумерации. |
| [setUseAltKinsokuLineBreakRules(boolean value)](#setUseAltKinsokuLineBreakRules-boolean-) | Используйте альтернативный набор восточноазиатских правил разрыва линии. |
| [setUseAnsiKerningPairs(boolean value)](#setUseAnsiKerningPairs-boolean-) | Используйте пары кернинга ANSI из шрифтов. |
| [setUseFELayout(boolean value)](#setUseFELayout-boolean-) | Не обходите восточноазиатский/сложный код макета сценария. |
| [setUseNormalStyleForList(boolean value)](#setUseNormalStyleForList-boolean-) | Не применять автоматически стиль абзаца списка к маркированному/нумерованному тексту. |
| [setUsePrinterMetrics(boolean value)](#setUsePrinterMetrics-boolean-) | Используйте показатели принтера для отображения документов. |
| [setUseSingleBorderforContiguousCells(boolean value)](#setUseSingleBorderforContiguousCells-boolean-) | Используйте упрощенные правила для конфликтов границ таблицы. |
| [setUseWord2002TableStyleRules(boolean value)](#setUseWord2002TableStyleRules-boolean-) | Эмулировать правила стиля таблицы Word 2002. |
| [setUseWord2010TableStyleRules(boolean value)](#setUseWord2010TableStyleRules-boolean-) |  |
| [setUseWord97LineBreakRules(boolean value)](#setUseWord97LineBreakRules-boolean-) | Эмуляция разрыва строки Word 97 в Восточной Азии. |
| [setWPJustification(boolean value)](#setWPJustification-boolean-) | Эмуляция выравнивания абзаца WordPerfect 6.x. |
| [setWPSpaceWidth(boolean value)](#setWPSpaceWidth-boolean-) | Указывает, следует ли устанавливать ширину пробела, как это делается в WordPerfect 5.x. |
| [setWrapTrailSpaces(boolean value)](#setWrapTrailSpaces-boolean-) | Завершающие пробелы переноса строк. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### getAdjustLineHeightInTable() {#getAdjustLineHeightInTable--}
```
public boolean getAdjustLineHeightInTable()
```


Добавьте шаг линии сетки документа к строкам в ячейках таблицы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getAlignTablesRowByRow() {#getAlignTablesRowByRow--}
```
public boolean getAlignTablesRowByRow()
```


Выравнивание строк таблицы независимо.

**Возвращает:**
boolean - соответствующее логическое значение.
### getAllowSpaceOfSameStyleInTable() {#getAllowSpaceOfSameStyleInTable--}
```
public boolean getAllowSpaceOfSameStyleInTable()
```


Разрешить контекстное расстояние между абзацами в таблицах.

**Возвращает:**
boolean - соответствующее логическое значение.
### getApplyBreakingRules() {#getApplyBreakingRules--}
```
public boolean getApplyBreakingRules()
```


Используйте устаревшие правила разбиения строк на эфиопском и амхарском языках.

**Возвращает:**
boolean - соответствующее логическое значение.
### getAutoSpaceLikeWord95() {#getAutoSpaceLikeWord95--}
```
public boolean getAutoSpaceLikeWord95()
```


Эмуляция полноширинного межсимвольного интервала Word 95.

**Возвращает:**
boolean - соответствующее логическое значение.
### getAutofitToFirstFixedWidthCell() {#getAutofitToFirstFixedWidthCell--}
```
public boolean getAutofitToFirstFixedWidthCell()
```


Разрешить столбцам таблицы превышать предпочтительную ширину составляющих ячеек. Параметр называется «Использовать правила автоподбора таблицы Word 2003» в пользовательском интерфейсе MS Word 2013. На самом деле это также влияет на то, как рассчитывается сетка для таблиц с фиксированным макетом (в некоторых случаях).

**Возвращает:**
boolean - соответствующее логическое значение.
### getBalanceSingleByteDoubleByteWidth() {#getBalanceSingleByteDoubleByteWidth--}
```
public boolean getBalanceSingleByteDoubleByteWidth()
```


Сбалансируйте однобайтовые и двухбайтовые символы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getCachedColBalance() {#getCachedColBalance--}
```
public boolean getCachedColBalance()
```


Используйте кэшированную информацию об абзацах для балансировки столбцов.

**Возвращает:**
boolean - соответствующее логическое значение.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getConvMailMergeEsc() {#getConvMailMergeEsc--}
```
public boolean getConvMailMergeEsc()
```


Рассматривайте разделитель кавычек с обратной косой чертой как две кавычки.

**Возвращает:**
boolean - соответствующее логическое значение.
### getDisableOpenTypeFontFormattingFeatures() {#getDisableOpenTypeFontFormattingFeatures--}
```
public boolean getDisableOpenTypeFontFormattingFeatures()
```




**Возвращает:**
логический
### getDisplayHangulFixedWidth() {#getDisplayHangulFixedWidth--}
```
public boolean getDisplayHangulFixedWidth()
```


Всегда используйте фиксированную ширину для символов хангыль.

**Возвращает:**
boolean - соответствующее логическое значение.
### getDoNotAutofitConstrainedTables() {#getDoNotAutofitConstrainedTables--}
```
public boolean getDoNotAutofitConstrainedTables()
```


Не используйте автоподгонку таблиц для размещения рядом с обернутыми объектами.

**Возвращает:**
boolean - соответствующее логическое значение.
### getDoNotBreakConstrainedForcedTable() {#getDoNotBreakConstrainedForcedTable--}
```
public boolean getDoNotBreakConstrainedForcedTable()
```


Не разбивайте строки таблицы вокруг плавающих таблиц.

**Возвращает:**
boolean - соответствующее логическое значение.
### getDoNotBreakWrappedTables() {#getDoNotBreakWrappedTables--}
```
public boolean getDoNotBreakWrappedTables()
```


Не позволяйте плавающим таблицам разбиваться на страницы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getDoNotExpandShiftReturn() {#getDoNotExpandShiftReturn--}
```
public boolean getDoNotExpandShiftReturn()
```


Не выравнивайте строки, заканчивающиеся мягким разрывом строки.

**Возвращает:**
boolean - соответствующее логическое значение.
### getDoNotLeaveBackslashAlone() {#getDoNotLeaveBackslashAlone--}
```
public boolean getDoNotLeaveBackslashAlone()
```


Преобразование обратной косой черты в знак иены при вводе.

**Возвращает:**
boolean - соответствующее логическое значение.
### getDoNotSnapToGridInCell() {#getDoNotSnapToGridInCell--}
```
public boolean getDoNotSnapToGridInCell()
```


Не привязываться к сетке документа в ячейках таблицы с объектами.

**Возвращает:**
boolean - соответствующее логическое значение.
### getDoNotSuppressIndentation() {#getDoNotSuppressIndentation--}
```
public boolean getDoNotSuppressIndentation()
```


Не игнорируйте плавающие объекты при расчете отступа абзаца.

**Возвращает:**
boolean - соответствующее логическое значение.
### getDoNotSuppressParagraphBorders() {#getDoNotSuppressParagraphBorders--}
```
public boolean getDoNotSuppressParagraphBorders()
```


Не подавлять границы абзаца рядом с фреймами.

**Возвращает:**
boolean - соответствующее логическое значение.
### getDoNotUseEastAsianBreakRules() {#getDoNotUseEastAsianBreakRules--}
```
public boolean getDoNotUseEastAsianBreakRules()
```


Не сжимайте сжимаемые символы при использовании сетки документа.

**Возвращает:**
boolean - соответствующее логическое значение.
### getDoNotUseHTMLParagraphAutoSpacing() {#getDoNotUseHTMLParagraphAutoSpacing--}
```
public boolean getDoNotUseHTMLParagraphAutoSpacing()
```


Используйте фиксированный интервал между абзацами для автоматической настройки HTML.

**Возвращает:**
boolean - соответствующее логическое значение.
### getDoNotUseIndentAsNumberingTabStop() {#getDoNotUseIndentAsNumberingTabStop--}
```
public boolean getDoNotUseIndentAsNumberingTabStop()
```


Игнорировать висячий отступ при создании позиции табуляции после нумерации.

**Возвращает:**
boolean - соответствующее логическое значение.
### getDoNotVertAlignCellWithSp() {#getDoNotVertAlignCellWithSp--}
```
public boolean getDoNotVertAlignCellWithSp()
```


Не выравнивайте по вертикали ячейки, содержащие плавающие объекты.

**Возвращает:**
boolean - соответствующее логическое значение.
### getDoNotVertAlignInTxbx() {#getDoNotVertAlignInTxbx--}
```
public boolean getDoNotVertAlignInTxbx()
```


Игнорировать вертикальное выравнивание в текстовых полях.

**Возвращает:**
boolean - соответствующее логическое значение.
### getDoNotWrapTextWithPunct() {#getDoNotWrapTextWithPunct--}
```
public boolean getDoNotWrapTextWithPunct()
```


Не разрешать висячие знаки препинания с сеткой символов.

**Возвращает:**
boolean - соответствующее логическое значение.
### getFootnoteLayoutLikeWW8() {#getFootnoteLayoutLikeWW8--}
```
public boolean getFootnoteLayoutLikeWW8()
```


Эмулировать размещение сносок Word 6.x/95/97.

**Возвращает:**
boolean - соответствующее логическое значение.
### getForgetLastTabAlignment() {#getForgetLastTabAlignment--}
```
public boolean getForgetLastTabAlignment()
```


Игнорировать ширину последней позиции табуляции при выравнивании абзаца, если он не выровнен по левому краю.

**Возвращает:**
boolean - соответствующее логическое значение.
### getGrowAutofit() {#getGrowAutofit--}
```
public boolean getGrowAutofit()
```


Разрешить автоподгонку таблиц к полям страницы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getLayoutRawTableWidth() {#getLayoutRawTableWidth--}
```
public boolean getLayoutRawTableWidth()
```


Игнорировать пробел перед таблицей при принятии решения о том, должна ли таблица оборачивать плавающий объект.

**Возвращает:**
boolean - соответствующее логическое значение.
### getLayoutTableRowsApart() {#getLayoutTableRowsApart--}
```
public boolean getLayoutTableRowsApart()
```


Разрешить строкам таблицы независимо оборачивать встроенные объекты.

**Возвращает:**
boolean - соответствующее логическое значение.
### getLineWrapLikeWord6() {#getLineWrapLikeWord6--}
```
public boolean getLineWrapLikeWord6()
```


Эмуляция переноса строк Word 6.0 для восточноазиатского текста.

**Возвращает:**
boolean - соответствующее логическое значение.
### getMWSmallCaps() {#getMWSmallCaps--}
```
public boolean getMWSmallCaps()
```


Эмулируйте Word 5.x для форматирования малых заглавных букв в Macintosh.

**Возвращает:**
boolean - соответствующее логическое значение.
### getNoColumnBalance() {#getNoColumnBalance--}
```
public boolean getNoColumnBalance()
```


Не балансируйте текстовые столбцы в разделе.

**Возвращает:**
boolean - соответствующее логическое значение.
### getNoExtraLineSpacing() {#getNoExtraLineSpacing--}
```
public boolean getNoExtraLineSpacing()
```


Не центрируйте содержимое на строках с точной высотой строки.

**Возвращает:**
boolean - соответствующее логическое значение.
### getNoLeading() {#getNoLeading--}
```
public boolean getNoLeading()
```


Не добавляйте интерлиньяж между строками текста.

**Возвращает:**
boolean - соответствующее логическое значение.
### getNoSpaceRaiseLower() {#getNoSpaceRaiseLower--}
```
public boolean getNoSpaceRaiseLower()
```


Не увеличивать высоту строки для приподнятого/пониженного текста.

**Возвращает:**
boolean - соответствующее логическое значение.
### getNoTabHangInd() {#getNoTabHangInd--}
```
public boolean getNoTabHangInd()
```


Не создавайте пользовательскую позицию табуляции для висячего отступа.

**Возвращает:**
boolean - соответствующее логическое значение.
### getOverrideTableStyleFontSizeAndJustification() {#getOverrideTableStyleFontSizeAndJustification--}
```
public boolean getOverrideTableStyleFontSizeAndJustification()
```


Указывает, как оценивается иерархия стилей документа.

**Возвращает:**
boolean - соответствующее логическое значение.
### getPrintBodyTextBeforeHeader() {#getPrintBodyTextBeforeHeader--}
```
public boolean getPrintBodyTextBeforeHeader()
```


Печатать основной текст перед содержимым верхнего/нижнего колонтитула.

**Возвращает:**
boolean - соответствующее логическое значение.
### getPrintColBlack() {#getPrintColBlack--}
```
public boolean getPrintColBlack()
```


Печатайте цвета как черно-белые без дизеринга.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSelectFldWithFirstOrLastChar() {#getSelectFldWithFirstOrLastChar--}
```
public boolean getSelectFldWithFirstOrLastChar()
```


Выберите поле, когда выбран первый или последний символ.

**Возвращает:**
boolean - соответствующее логическое значение.
### getShapeLayoutLikeWW8() {#getShapeLayoutLikeWW8--}
```
public boolean getShapeLayoutLikeWW8()
```


Эмуляция переноса текста Word 97 вокруг плавающих объектов.

**Возвращает:**
boolean - соответствующее логическое значение.
### getShowBreaksInFrames() {#getShowBreaksInFrames--}
```
public boolean getShowBreaksInFrames()
```


Отображение разрывов страниц/столбцов во фреймах.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSpaceForUL() {#getSpaceForUL--}
```
public boolean getSpaceForUL()
```


Добавьте дополнительное пространство ниже базовой линии для подчеркнутого восточноазиатского текста.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSpacingInWholePoints() {#getSpacingInWholePoints--}
```
public boolean getSpacingInWholePoints()
```


Расширить/сжать текст только по целым точкам.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSplitPgBreakAndParaMark() {#getSplitPgBreakAndParaMark--}
```
public boolean getSplitPgBreakAndParaMark()
```


Всегда перемещайте метку абзаца на страницу после разрыва страницы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSubFontBySize() {#getSubFontBySize--}
```
public boolean getSubFontBySize()
```


Увеличьте приоритет размера шрифта при замене шрифта.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSuppressBottomSpacing() {#getSuppressBottomSpacing--}
```
public boolean getSuppressBottomSpacing()
```


Игнорировать точную высоту строки для последней строки на странице.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSuppressSpBfAfterPgBrk() {#getSuppressSpBfAfterPgBrk--}
```
public boolean getSuppressSpBfAfterPgBrk()
```


Не используйте пробел перед первой строкой после разрыва страницы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSuppressSpacingAtTopOfPage() {#getSuppressSpacingAtTopOfPage--}
```
public boolean getSuppressSpacingAtTopOfPage()
```


Игнорировать минимальную высоту строки для первой строки на странице.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSuppressTopSpacing() {#getSuppressTopSpacing--}
```
public boolean getSuppressTopSpacing()
```


Игнорировать минимальную и точную высоту строки для первой строки на странице.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSuppressTopSpacingWP() {#getSuppressTopSpacingWP--}
```
public boolean getSuppressTopSpacingWP()
```


Эмуляция межстрочного интервала WordPerfect 5.x.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSwapBordersFacingPgs() {#getSwapBordersFacingPgs--}
```
public boolean getSwapBordersFacingPgs()
```


Поменять местами границы абзаца на страницах с нечетными номерами.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning() {#getSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning--}
```
public boolean getSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning()
```




**Возвращает:**
логический
### getTransparentMetafiles() {#getTransparentMetafiles--}
```
public boolean getTransparentMetafiles()
```


Указывает, что область за изображениями метафайла не очищается.

**Возвращает:**
boolean - соответствующее логическое значение.
### getTruncateFontHeightsLikeWP6() {#getTruncateFontHeightsLikeWP6--}
```
public boolean getTruncateFontHeightsLikeWP6()
```


Эмуляция вычисления высоты шрифта WordPerfect 6.x.

**Возвращает:**
boolean - соответствующее логическое значение.
### getUICompat97To2003() {#getUICompat97To2003--}
```
public boolean getUICompat97To2003()
```


**True** чтобы отключить функциональность пользовательского интерфейса, несовместимую с Word97-2003. Значение по умолчанию**false** . Управляет параметром совместимости Word97-2003, который отключает функции пользовательского интерфейса, несовместимые с Word97-2003. Когда**true**, 'w:uiCompat97To2003' XML-элемент записывается в '\\слово\ Часть пакета документа \settings.xml. Значение по умолчанию**false** . При установке на**false**, этот элемент не записывается. Технически это свойство не является частью параметров совместимости, но мы разместили его здесь для удобства API.

**Возвращает:**
boolean - соответствующее логическое значение.
### getUlTrailSpace() {#getUlTrailSpace--}
```
public boolean getUlTrailSpace()
```


Подчеркните все конечные пробелы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getUnderlineTabInNumList() {#getUnderlineTabInNumList--}
```
public boolean getUnderlineTabInNumList()
```


Подчеркните следующий символ после нумерации.

**Возвращает:**
boolean - соответствующее логическое значение.
### getUseAltKinsokuLineBreakRules() {#getUseAltKinsokuLineBreakRules--}
```
public boolean getUseAltKinsokuLineBreakRules()
```


Используйте альтернативный набор восточноазиатских правил разрыва линии.

**Возвращает:**
boolean - соответствующее логическое значение.
### getUseAnsiKerningPairs() {#getUseAnsiKerningPairs--}
```
public boolean getUseAnsiKerningPairs()
```


Используйте пары кернинга ANSI из шрифтов.

**Возвращает:**
boolean - соответствующее логическое значение.
### getUseFELayout() {#getUseFELayout--}
```
public boolean getUseFELayout()
```


Не обходите восточноазиатский/сложный код макета сценария.

**Возвращает:**
boolean - соответствующее логическое значение.
### getUseNormalStyleForList() {#getUseNormalStyleForList--}
```
public boolean getUseNormalStyleForList()
```


Не применять автоматически стиль абзаца списка к маркированному/нумерованному тексту.

**Возвращает:**
boolean - соответствующее логическое значение.
### getUsePrinterMetrics() {#getUsePrinterMetrics--}
```
public boolean getUsePrinterMetrics()
```


Используйте показатели принтера для отображения документов. Показатели принтера могут различаться в зависимости от используемых драйверов. Например, Windows «Microsoft OpenXPS Class Driver 2» и «Microsoft Print to PDF» предоставляют немного разные показатели. Таким образом, итоговый макет документа может измениться, если этот параметр включен.

**Возвращает:**
boolean - соответствующее логическое значение.
### getUseSingleBorderforContiguousCells() {#getUseSingleBorderforContiguousCells--}
```
public boolean getUseSingleBorderforContiguousCells()
```


Используйте упрощенные правила для конфликтов границ таблицы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getUseWord2002TableStyleRules() {#getUseWord2002TableStyleRules--}
```
public boolean getUseWord2002TableStyleRules()
```


Эмулировать правила стиля таблицы Word 2002.

**Возвращает:**
boolean - соответствующее логическое значение.
### getUseWord2010TableStyleRules() {#getUseWord2010TableStyleRules--}
```
public boolean getUseWord2010TableStyleRules()
```




**Возвращает:**
логический
### getUseWord97LineBreakRules() {#getUseWord97LineBreakRules--}
```
public boolean getUseWord97LineBreakRules()
```


Эмуляция разрыва строки Word 97 в Восточной Азии.

**Возвращает:**
boolean - соответствующее логическое значение.
### getWPJustification() {#getWPJustification--}
```
public boolean getWPJustification()
```


Эмуляция выравнивания абзаца WordPerfect 6.x.

**Возвращает:**
boolean - соответствующее логическое значение.
### getWPSpaceWidth() {#getWPSpaceWidth--}
```
public boolean getWPSpaceWidth()
```


Указывает, следует ли устанавливать ширину пробела, как это делается в WordPerfect 5.x.

**Возвращает:**
boolean - соответствующее логическое значение.
### getWrapTrailSpaces() {#getWrapTrailSpaces--}
```
public boolean getWrapTrailSpaces()
```


Завершающие пробелы переноса строк.

**Возвращает:**
boolean - соответствующее логическое значение.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### optimizeFor(int version) {#optimizeFor-int-}
```
public void optimizeFor(int version)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| version | int |  |

### setAdjustLineHeightInTable(boolean value) {#setAdjustLineHeightInTable-boolean-}
```
public void setAdjustLineHeightInTable(boolean value)
```


Добавьте шаг линии сетки документа к строкам в ячейках таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setAlignTablesRowByRow(boolean value) {#setAlignTablesRowByRow-boolean-}
```
public void setAlignTablesRowByRow(boolean value)
```


Выравнивание строк таблицы независимо.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setAllowSpaceOfSameStyleInTable(boolean value) {#setAllowSpaceOfSameStyleInTable-boolean-}
```
public void setAllowSpaceOfSameStyleInTable(boolean value)
```


Разрешить контекстное расстояние между абзацами в таблицах.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setApplyBreakingRules(boolean value) {#setApplyBreakingRules-boolean-}
```
public void setApplyBreakingRules(boolean value)
```


Используйте устаревшие правила разбиения строк на эфиопском и амхарском языках.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setAutoSpaceLikeWord95(boolean value) {#setAutoSpaceLikeWord95-boolean-}
```
public void setAutoSpaceLikeWord95(boolean value)
```


Эмуляция полноширинного межсимвольного интервала Word 95.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setAutofitToFirstFixedWidthCell(boolean value) {#setAutofitToFirstFixedWidthCell-boolean-}
```
public void setAutofitToFirstFixedWidthCell(boolean value)
```


Разрешить столбцам таблицы превышать предпочтительную ширину составляющих ячеек. Параметр называется «Использовать правила автоподбора таблицы Word 2003» в пользовательском интерфейсе MS Word 2013. На самом деле это также влияет на то, как рассчитывается сетка для таблиц с фиксированным макетом (в некоторых случаях).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setBalanceSingleByteDoubleByteWidth(boolean value) {#setBalanceSingleByteDoubleByteWidth-boolean-}
```
public void setBalanceSingleByteDoubleByteWidth(boolean value)
```


Сбалансируйте однобайтовые и двухбайтовые символы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setCachedColBalance(boolean value) {#setCachedColBalance-boolean-}
```
public void setCachedColBalance(boolean value)
```


Используйте кэшированную информацию об абзацах для балансировки столбцов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setConvMailMergeEsc(boolean value) {#setConvMailMergeEsc-boolean-}
```
public void setConvMailMergeEsc(boolean value)
```


Рассматривайте разделитель кавычек с обратной косой чертой как две кавычки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDisableOpenTypeFontFormattingFeatures(boolean value) {#setDisableOpenTypeFontFormattingFeatures-boolean-}
```
public void setDisableOpenTypeFontFormattingFeatures(boolean value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  |

### setDisplayHangulFixedWidth(boolean value) {#setDisplayHangulFixedWidth-boolean-}
```
public void setDisplayHangulFixedWidth(boolean value)
```


Всегда используйте фиксированную ширину для символов хангыль.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDoNotAutofitConstrainedTables(boolean value) {#setDoNotAutofitConstrainedTables-boolean-}
```
public void setDoNotAutofitConstrainedTables(boolean value)
```


Не используйте автоподгонку таблиц для размещения рядом с обернутыми объектами.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDoNotBreakConstrainedForcedTable(boolean value) {#setDoNotBreakConstrainedForcedTable-boolean-}
```
public void setDoNotBreakConstrainedForcedTable(boolean value)
```


Не разбивайте строки таблицы вокруг плавающих таблиц.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDoNotBreakWrappedTables(boolean value) {#setDoNotBreakWrappedTables-boolean-}
```
public void setDoNotBreakWrappedTables(boolean value)
```


Не позволяйте плавающим таблицам разбиваться на страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDoNotExpandShiftReturn(boolean value) {#setDoNotExpandShiftReturn-boolean-}
```
public void setDoNotExpandShiftReturn(boolean value)
```


Не выравнивайте строки, заканчивающиеся мягким разрывом строки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDoNotLeaveBackslashAlone(boolean value) {#setDoNotLeaveBackslashAlone-boolean-}
```
public void setDoNotLeaveBackslashAlone(boolean value)
```


Преобразование обратной косой черты в знак иены при вводе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDoNotSnapToGridInCell(boolean value) {#setDoNotSnapToGridInCell-boolean-}
```
public void setDoNotSnapToGridInCell(boolean value)
```


Не привязываться к сетке документа в ячейках таблицы с объектами.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDoNotSuppressIndentation(boolean value) {#setDoNotSuppressIndentation-boolean-}
```
public void setDoNotSuppressIndentation(boolean value)
```


Не игнорируйте плавающие объекты при расчете отступа абзаца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDoNotSuppressParagraphBorders(boolean value) {#setDoNotSuppressParagraphBorders-boolean-}
```
public void setDoNotSuppressParagraphBorders(boolean value)
```


Не подавлять границы абзаца рядом с фреймами.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDoNotUseEastAsianBreakRules(boolean value) {#setDoNotUseEastAsianBreakRules-boolean-}
```
public void setDoNotUseEastAsianBreakRules(boolean value)
```


Не сжимайте сжимаемые символы при использовании сетки документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDoNotUseHTMLParagraphAutoSpacing(boolean value) {#setDoNotUseHTMLParagraphAutoSpacing-boolean-}
```
public void setDoNotUseHTMLParagraphAutoSpacing(boolean value)
```


Используйте фиксированный интервал между абзацами для автоматической настройки HTML.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDoNotUseIndentAsNumberingTabStop(boolean value) {#setDoNotUseIndentAsNumberingTabStop-boolean-}
```
public void setDoNotUseIndentAsNumberingTabStop(boolean value)
```


Игнорировать висячий отступ при создании позиции табуляции после нумерации.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDoNotVertAlignCellWithSp(boolean value) {#setDoNotVertAlignCellWithSp-boolean-}
```
public void setDoNotVertAlignCellWithSp(boolean value)
```


Не выравнивайте по вертикали ячейки, содержащие плавающие объекты.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDoNotVertAlignInTxbx(boolean value) {#setDoNotVertAlignInTxbx-boolean-}
```
public void setDoNotVertAlignInTxbx(boolean value)
```


Игнорировать вертикальное выравнивание в текстовых полях.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDoNotWrapTextWithPunct(boolean value) {#setDoNotWrapTextWithPunct-boolean-}
```
public void setDoNotWrapTextWithPunct(boolean value)
```


Не разрешать висячие знаки препинания с сеткой символов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setFootnoteLayoutLikeWW8(boolean value) {#setFootnoteLayoutLikeWW8-boolean-}
```
public void setFootnoteLayoutLikeWW8(boolean value)
```


Эмулировать размещение сносок Word 6.x/95/97.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setForgetLastTabAlignment(boolean value) {#setForgetLastTabAlignment-boolean-}
```
public void setForgetLastTabAlignment(boolean value)
```


Игнорировать ширину последней позиции табуляции при выравнивании абзаца, если он не выровнен по левому краю.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setGrowAutofit(boolean value) {#setGrowAutofit-boolean-}
```
public void setGrowAutofit(boolean value)
```


Разрешить автоподгонку таблиц к полям страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setLayoutRawTableWidth(boolean value) {#setLayoutRawTableWidth-boolean-}
```
public void setLayoutRawTableWidth(boolean value)
```


Игнорировать пробел перед таблицей при принятии решения о том, должна ли таблица оборачивать плавающий объект.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setLayoutTableRowsApart(boolean value) {#setLayoutTableRowsApart-boolean-}
```
public void setLayoutTableRowsApart(boolean value)
```


Разрешить строкам таблицы независимо оборачивать встроенные объекты.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setLineWrapLikeWord6(boolean value) {#setLineWrapLikeWord6-boolean-}
```
public void setLineWrapLikeWord6(boolean value)
```


Эмуляция переноса строк Word 6.0 для восточноазиатского текста.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setMWSmallCaps(boolean value) {#setMWSmallCaps-boolean-}
```
public void setMWSmallCaps(boolean value)
```


Эмулируйте Word 5.x для форматирования малых заглавных букв в Macintosh.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setNoColumnBalance(boolean value) {#setNoColumnBalance-boolean-}
```
public void setNoColumnBalance(boolean value)
```


Не балансируйте текстовые столбцы в разделе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setNoExtraLineSpacing(boolean value) {#setNoExtraLineSpacing-boolean-}
```
public void setNoExtraLineSpacing(boolean value)
```


Не центрируйте содержимое на строках с точной высотой строки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setNoLeading(boolean value) {#setNoLeading-boolean-}
```
public void setNoLeading(boolean value)
```


Не добавляйте интерлиньяж между строками текста.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setNoSpaceRaiseLower(boolean value) {#setNoSpaceRaiseLower-boolean-}
```
public void setNoSpaceRaiseLower(boolean value)
```


Не увеличивать высоту строки для приподнятого/пониженного текста.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setNoTabHangInd(boolean value) {#setNoTabHangInd-boolean-}
```
public void setNoTabHangInd(boolean value)
```


Не создавайте пользовательскую позицию табуляции для висячего отступа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setOverrideTableStyleFontSizeAndJustification(boolean value) {#setOverrideTableStyleFontSizeAndJustification-boolean-}
```
public void setOverrideTableStyleFontSizeAndJustification(boolean value)
```


Указывает, как оценивается иерархия стилей документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setPrintBodyTextBeforeHeader(boolean value) {#setPrintBodyTextBeforeHeader-boolean-}
```
public void setPrintBodyTextBeforeHeader(boolean value)
```


Печатать основной текст перед содержимым верхнего/нижнего колонтитула.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setPrintColBlack(boolean value) {#setPrintColBlack-boolean-}
```
public void setPrintColBlack(boolean value)
```


Печатайте цвета как черно-белые без дизеринга.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSelectFldWithFirstOrLastChar(boolean value) {#setSelectFldWithFirstOrLastChar-boolean-}
```
public void setSelectFldWithFirstOrLastChar(boolean value)
```


Выберите поле, когда выбран первый или последний символ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setShapeLayoutLikeWW8(boolean value) {#setShapeLayoutLikeWW8-boolean-}
```
public void setShapeLayoutLikeWW8(boolean value)
```


Эмуляция переноса текста Word 97 вокруг плавающих объектов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setShowBreaksInFrames(boolean value) {#setShowBreaksInFrames-boolean-}
```
public void setShowBreaksInFrames(boolean value)
```


Отображение разрывов страниц/столбцов во фреймах.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSpaceForUL(boolean value) {#setSpaceForUL-boolean-}
```
public void setSpaceForUL(boolean value)
```


Добавьте дополнительное пространство ниже базовой линии для подчеркнутого восточноазиатского текста.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSpacingInWholePoints(boolean value) {#setSpacingInWholePoints-boolean-}
```
public void setSpacingInWholePoints(boolean value)
```


Расширить/сжать текст только по целым точкам.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSplitPgBreakAndParaMark(boolean value) {#setSplitPgBreakAndParaMark-boolean-}
```
public void setSplitPgBreakAndParaMark(boolean value)
```


Всегда перемещайте метку абзаца на страницу после разрыва страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSubFontBySize(boolean value) {#setSubFontBySize-boolean-}
```
public void setSubFontBySize(boolean value)
```


Увеличьте приоритет размера шрифта при замене шрифта.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSuppressBottomSpacing(boolean value) {#setSuppressBottomSpacing-boolean-}
```
public void setSuppressBottomSpacing(boolean value)
```


Игнорировать точную высоту строки для последней строки на странице.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSuppressSpBfAfterPgBrk(boolean value) {#setSuppressSpBfAfterPgBrk-boolean-}
```
public void setSuppressSpBfAfterPgBrk(boolean value)
```


Не используйте пробел перед первой строкой после разрыва страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSuppressSpacingAtTopOfPage(boolean value) {#setSuppressSpacingAtTopOfPage-boolean-}
```
public void setSuppressSpacingAtTopOfPage(boolean value)
```


Игнорировать минимальную высоту строки для первой строки на странице.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSuppressTopSpacing(boolean value) {#setSuppressTopSpacing-boolean-}
```
public void setSuppressTopSpacing(boolean value)
```


Игнорировать минимальную и точную высоту строки для первой строки на странице.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSuppressTopSpacingWP(boolean value) {#setSuppressTopSpacingWP-boolean-}
```
public void setSuppressTopSpacingWP(boolean value)
```


Эмуляция межстрочного интервала WordPerfect 5.x.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSwapBordersFacingPgs(boolean value) {#setSwapBordersFacingPgs-boolean-}
```
public void setSwapBordersFacingPgs(boolean value)
```


Поменять местами границы абзаца на страницах с нечетными номерами.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning(boolean value) {#setSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning-boolean-}
```
public void setSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning(boolean value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  |

### setTransparentMetafiles(boolean value) {#setTransparentMetafiles-boolean-}
```
public void setTransparentMetafiles(boolean value)
```


Указывает, что область за изображениями метафайла не очищается.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setTruncateFontHeightsLikeWP6(boolean value) {#setTruncateFontHeightsLikeWP6-boolean-}
```
public void setTruncateFontHeightsLikeWP6(boolean value)
```


Эмуляция вычисления высоты шрифта WordPerfect 6.x.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setUICompat97To2003(boolean value) {#setUICompat97To2003-boolean-}
```
public void setUICompat97To2003(boolean value)
```


**True** чтобы отключить функциональность пользовательского интерфейса, несовместимую с Word97-2003. Значение по умолчанию**false** . Управляет параметром совместимости Word97-2003, который отключает функции пользовательского интерфейса, несовместимые с Word97-2003. Когда**true**, 'w:uiCompat97To2003' XML-элемент записывается в '\\слово\ Часть пакета документа \settings.xml. Значение по умолчанию**false** . При установке на**false**, этот элемент не записывается. Технически это свойство не является частью параметров совместимости, но мы разместили его здесь для удобства API.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setUlTrailSpace(boolean value) {#setUlTrailSpace-boolean-}
```
public void setUlTrailSpace(boolean value)
```


Подчеркните все конечные пробелы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setUnderlineTabInNumList(boolean value) {#setUnderlineTabInNumList-boolean-}
```
public void setUnderlineTabInNumList(boolean value)
```


Подчеркните следующий символ после нумерации.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setUseAltKinsokuLineBreakRules(boolean value) {#setUseAltKinsokuLineBreakRules-boolean-}
```
public void setUseAltKinsokuLineBreakRules(boolean value)
```


Используйте альтернативный набор восточноазиатских правил разрыва линии.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setUseAnsiKerningPairs(boolean value) {#setUseAnsiKerningPairs-boolean-}
```
public void setUseAnsiKerningPairs(boolean value)
```


Используйте пары кернинга ANSI из шрифтов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setUseFELayout(boolean value) {#setUseFELayout-boolean-}
```
public void setUseFELayout(boolean value)
```


Не обходите восточноазиатский/сложный код макета сценария.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setUseNormalStyleForList(boolean value) {#setUseNormalStyleForList-boolean-}
```
public void setUseNormalStyleForList(boolean value)
```


Не применять автоматически стиль абзаца списка к маркированному/нумерованному тексту.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setUsePrinterMetrics(boolean value) {#setUsePrinterMetrics-boolean-}
```
public void setUsePrinterMetrics(boolean value)
```


Используйте показатели принтера для отображения документов. Показатели принтера могут различаться в зависимости от используемых драйверов. Например, Windows «Microsoft OpenXPS Class Driver 2» и «Microsoft Print to PDF» предоставляют немного разные показатели. Таким образом, итоговый макет документа может измениться, если этот параметр включен.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setUseSingleBorderforContiguousCells(boolean value) {#setUseSingleBorderforContiguousCells-boolean-}
```
public void setUseSingleBorderforContiguousCells(boolean value)
```


Используйте упрощенные правила для конфликтов границ таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setUseWord2002TableStyleRules(boolean value) {#setUseWord2002TableStyleRules-boolean-}
```
public void setUseWord2002TableStyleRules(boolean value)
```


Эмулировать правила стиля таблицы Word 2002.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setUseWord2010TableStyleRules(boolean value) {#setUseWord2010TableStyleRules-boolean-}
```
public void setUseWord2010TableStyleRules(boolean value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  |

### setUseWord97LineBreakRules(boolean value) {#setUseWord97LineBreakRules-boolean-}
```
public void setUseWord97LineBreakRules(boolean value)
```


Эмуляция разрыва строки Word 97 в Восточной Азии.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setWPJustification(boolean value) {#setWPJustification-boolean-}
```
public void setWPJustification(boolean value)
```


Эмуляция выравнивания абзаца WordPerfect 6.x.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setWPSpaceWidth(boolean value) {#setWPSpaceWidth-boolean-}
```
public void setWPSpaceWidth(boolean value)
```


Указывает, следует ли устанавливать ширину пробела, как это делается в WordPerfect 5.x.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setWrapTrailSpaces(boolean value) {#setWrapTrailSpaces-boolean-}
```
public void setWrapTrailSpaces(boolean value)
```


Завершающие пробелы переноса строк.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

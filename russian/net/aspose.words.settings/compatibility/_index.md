---
title: Compatibility Enum
linktitle: Compatibility
articleTitle: Compatibility
second_title: Aspose.Words для .NET
description: Изучите перечисление Aspose.Words.Settings.Compatibility, чтобы открыть мощные параметры совместимости для бесперебойной обработки документов и повышения производительности.
type: docs
weight: 6600
url: /ru/net/aspose.words.settings/compatibility/
---
## Compatibility enumeration

Указывает имена параметров совместимости.

```csharp
public enum Compatibility
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| NoTabHangInd | `0` | Без отступа для подвешивания табуляции |
| NoSpaceRaiseLower | `1` | Нет пробела Поднять Опустить |
| SuppressSpBfAfterPgBrk | `2` | Подавить пробел перед разрывом абзаца |
| WrapTrailSpaces | `3` | Перенести конечные пробелы |
| PrintColBlack | `4` | Фон столбца печати |
| NoColumnBalance | `5` | Нет балансировки столбцов |
| ConvMailMergeEsc | `6` | Преобразование экранов слияния почты |
| SuppressTopSpacing | `7` | Подавить верхний интервал |
| UseSingleBorderforContiguousCells | `8` | Использовать одинарную границу для смежных ячеек |
| TransparentMetafiles | `9` | Прозрачные метафайлы |
| ShowBreaksInFrames | `10` | Показывать разрывы в кадрах |
| SwapBordersOddFacingPgs | `11` | Поменять местами границы на нечетных страницах |
| DoNotLeaveBackslashAlone | `12` | Не оставляйте обратную косую черту в покое |
| DoNotExpandOnShiftReturn | `13` | Не расширять при нажатии клавиши Shift Return |
| UlTrailSpace | `14` | Подчеркивание конечного пробела |
| BalanceSingleByteDoubleByteWidth | `15` | Баланс однобайтовой и двухбайтовой ширины |
| SuppressTopSpacingAtTopOfPage | `16` | Подавить межстрочный интервал в WordPerfect |
| SpacingInWholePoints | `17` | Интервал в целых точках |
| PrintBodyTextBeforeHeader | `18` | Печатать основной текст перед заголовком |
| NoLeading | `19` | Нет Ведущего |
| SpaceForUL | `20` | Место для подчеркивания |
| MWSmallCaps | `21` | MW Малые Капители |
| SuppressTopLineSpacingWP | `22` | Подавить межстрочный интервал в WordPerfect |
| TruncateFontHeightLikeWP6 | `23` | Усечение высоты шрифта, как у WordPerfect 6 |
| SubFontBySize | `24` | Заменить шрифт по размеру |
| LineWrapLikeWord6 | `25` | Перенос строки, как в слове 6 |
| DoNotSuppressParagraphBorder | `26` | Не подавлять границу абзаца |
| NoExtraLineSpacing | `27` | Без дополнительного межстрочного интервала |
| SuppressBottomSpacing | `28` | Подавить нижний интервал |
| WPSpaceWidth | `29` | Ширина пробела WordPerfect |
| WPJustification | `30` | WordPerfect Выравнивание |
| UsePrinterMetrics | `31` | Использовать метрики принтера |
| ShapeLayoutLikeWW8 | `32` | Форма макета как Word 2000 |
| FootnoteLayoutLikeWW8 | `33` | Макет сноски как в Word 2000 |
| DoNotUseHtmlParagraphAutoSpacing | `34` | Не использовать автоматический интервал между абзацами HTML |
| AdjustLineHeightInTable | `35` | Настроить высоту строки в таблице |
| ForgetLastTabAlignment | `36` | Забыть последнее выравнивание табуляции |
| AutoSpaceLikeWord95 | `37` | Автоматический пробел, как в слове 95 |
| AlignTableRowByRow | `38` | Выровнять строки таблицы по правилу |
| LayoutRawTableWidth | `39` | Ширина необработанной таблицы макета |
| LayoutTableRowsApart | `40` | Макет таблицы Строки врозь |
| UseWord97LineBreakRules | `41` | Используйте правила переноса строк Word 97 |
| DoNotBreakWrappedTables | `42` | Не разбивайте упакованные таблицы |
| doNotSnapToGridInCell | `43` | Не привязываться к сетке в ячейках |
| SelectFldWithFirstOrLastChar | `44` | Выберите поле с первым или последним символом |
| ApplyBreakingRules | `45` | Применить правила нарушения |
| DoNotWrapTextWithPunct | `46` | Не переносить текст знаками пунктуации |
| DoNotUseEastAsianBreakRules | `47` | Не используйте правила перерыва в Восточной Азии |
| UseWord2002TableStyleRules | `48` | Использовать правила стиля таблиц Word 2002 |
| GrowAutofit | `49` | Вырасти AutoFit |
| UseNormalStyleForList | `50` | Использовать обычный стиль для списка |
| DoNotUseIndentAsNumberingTabStop | `51` | Не использовать отступ в качестве нумерации Табуляция |
| UseAltKinsokuLineBreakRules | `52` | Использовать правила разрыва строки Alt Kinsoku |
| AllowSpaceOfSameStyleInTable | `53` | Разрешить пробелы того же стиля в таблице |
| DoNotSuppressIndentation | `54` | Не подавлять отступы |
| DoNotAutofitConstrainedTables | `55` | Не применять автоподбор для таблиц с ограничениями |
| AutofitToFirstFixedWidthCell | `56` | Автоподбор по первой ячейке фиксированной ширины |
| UnderlineTabInNumList | `57` | Подчеркивание табуляции в нумерованном списке |
| DisplayHangulFixedWidth | `58` | Отображение фиксированной ширины хангыля |
| SplitPgBreakAndParaMark | `59` | Разделить разрыв страницы и знак абзаца |
| DoNotVertAlignCellWithSp | `60` | Не выравнивать ячейку по вертикали с интервалом |
| DoNotBreakConstrainedForcedTable | `61` | Не разрушать ограниченные принудительные таблицы |
| DoNotVertAlignInTxbx | `62` | Не выравнивать по вертикали в текстовых полях |
| UseAnsiKerningPairs | `63` | Использовать пары кернинга ANSI |
| CachedColBalance | `64` | Балансировка кэшированных столбцов |
| UseFELayout | `65` | Использовать макет Дальнего Востока |
| UICompat97To2003 | `66` | Режим совместимости пользовательского интерфейса от Word 97 до Word 2003 |
| OverrideTableStyleFontSizeAndJustification | `67` | Переопределить размер шрифта и выравнивание стиля таблицы |
| DisableOpenTypeFontFormattingFeatures | `68` | Отключить функции форматирования шрифтов OpenType |
| SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning | `69` | Поменять местами внутреннюю и внешнюю стороны для зеркальных отступов и относительного позиционирования |
| UseWord2010TableStyleRules | `70` | Использовать правила стиля таблиц Word 2010 |

## Примеры

Показывает, как оптимизировать документ для разных версий Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Этот объект содержит обширный список флагов, уникальных для каждого документа
    // которые позволяют нам обеспечить обратную совместимость со старыми версиями Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Распечатать настройки по умолчанию для пустого документа.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Доступ к этим настройкам в Microsoft Word можно получить через «Файл» -> «Параметры» -> «Дополнительно» -> «Параметры совместимости для...».
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Мы можем использовать метод OptimizeFor для обеспечения оптимальной совместимости с конкретной версией Microsoft Word.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Группирует все флаги в объекте параметров совместимости документа по состоянию, затем печатает каждую группу.
/// </summary>
private static void PrintCompatibilityOptions(CompatibilityOptions options)
{
    IList<string> enabledOptions = new List<string>();
    IList<string> disabledOptions = new List<string>();
    AddOptionName(options.AdjustLineHeightInTable, "AdjustLineHeightInTable", enabledOptions, disabledOptions);
    AddOptionName(options.AlignTablesRowByRow, "AlignTablesRowByRow", enabledOptions, disabledOptions);
    AddOptionName(options.AllowSpaceOfSameStyleInTable, "AllowSpaceOfSameStyleInTable", enabledOptions, disabledOptions);
    AddOptionName(options.ApplyBreakingRules, "ApplyBreakingRules", enabledOptions, disabledOptions);
    AddOptionName(options.AutoSpaceLikeWord95, "AutoSpaceLikeWord95", enabledOptions, disabledOptions);
    AddOptionName(options.AutofitToFirstFixedWidthCell, "AutofitToFirstFixedWidthCell", enabledOptions, disabledOptions);
    AddOptionName(options.BalanceSingleByteDoubleByteWidth, "BalanceSingleByteDoubleByteWidth", enabledOptions, disabledOptions);
    AddOptionName(options.CachedColBalance, "CachedColBalance", enabledOptions, disabledOptions);
    AddOptionName(options.ConvMailMergeEsc, "ConvMailMergeEsc", enabledOptions, disabledOptions);
    AddOptionName(options.DisableOpenTypeFontFormattingFeatures, "DisableOpenTypeFontFormattingFeatures", enabledOptions, disabledOptions);
    AddOptionName(options.DisplayHangulFixedWidth, "DisplayHangulFixedWidth", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotAutofitConstrainedTables, "DoNotAutofitConstrainedTables", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotBreakConstrainedForcedTable, "DoNotBreakConstrainedForcedTable", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotBreakWrappedTables, "DoNotBreakWrappedTables", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotExpandShiftReturn, "DoNotExpandShiftReturn", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotLeaveBackslashAlone, "DoNotLeaveBackslashAlone", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotSnapToGridInCell, "DoNotSnapToGridInCell", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotSuppressIndentation, "DoNotSnapToGridInCell", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotSuppressParagraphBorders, "DoNotSuppressParagraphBorders", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotUseEastAsianBreakRules, "DoNotUseEastAsianBreakRules", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotUseHTMLParagraphAutoSpacing, "DoNotUseHTMLParagraphAutoSpacing", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotUseIndentAsNumberingTabStop, "DoNotUseIndentAsNumberingTabStop", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotVertAlignCellWithSp, "DoNotVertAlignCellWithSp", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotVertAlignInTxbx, "DoNotVertAlignInTxbx", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotWrapTextWithPunct, "DoNotWrapTextWithPunct", enabledOptions, disabledOptions);
    AddOptionName(options.FootnoteLayoutLikeWW8, "FootnoteLayoutLikeWW8", enabledOptions, disabledOptions);
    AddOptionName(options.ForgetLastTabAlignment, "ForgetLastTabAlignment", enabledOptions, disabledOptions);
    AddOptionName(options.GrowAutofit, "GrowAutofit", enabledOptions, disabledOptions);
    AddOptionName(options.LayoutRawTableWidth, "LayoutRawTableWidth", enabledOptions, disabledOptions);
    AddOptionName(options.LayoutTableRowsApart, "LayoutTableRowsApart", enabledOptions, disabledOptions);
    AddOptionName(options.LineWrapLikeWord6, "LineWrapLikeWord6", enabledOptions, disabledOptions);
    AddOptionName(options.MWSmallCaps, "MWSmallCaps", enabledOptions, disabledOptions);
    AddOptionName(options.NoColumnBalance, "NoColumnBalance", enabledOptions, disabledOptions);
    AddOptionName(options.NoExtraLineSpacing, "NoExtraLineSpacing", enabledOptions, disabledOptions);
    AddOptionName(options.NoLeading, "NoLeading", enabledOptions, disabledOptions);
    AddOptionName(options.NoSpaceRaiseLower, "NoSpaceRaiseLower", enabledOptions, disabledOptions);
    AddOptionName(options.NoTabHangInd, "NoTabHangInd", enabledOptions, disabledOptions);
    AddOptionName(options.OverrideTableStyleFontSizeAndJustification, "OverrideTableStyleFontSizeAndJustification", enabledOptions, disabledOptions);
    AddOptionName(options.PrintBodyTextBeforeHeader, "PrintBodyTextBeforeHeader", enabledOptions, disabledOptions);
    AddOptionName(options.PrintColBlack, "PrintColBlack", enabledOptions, disabledOptions);
    AddOptionName(options.SelectFldWithFirstOrLastChar, "SelectFldWithFirstOrLastChar", enabledOptions, disabledOptions);
    AddOptionName(options.ShapeLayoutLikeWW8, "ShapeLayoutLikeWW8", enabledOptions, disabledOptions);
    AddOptionName(options.ShowBreaksInFrames, "ShowBreaksInFrames", enabledOptions, disabledOptions);
    AddOptionName(options.SpaceForUL, "SpaceForUL", enabledOptions, disabledOptions);
    AddOptionName(options.SpacingInWholePoints, "SpacingInWholePoints", enabledOptions, disabledOptions);
    AddOptionName(options.SplitPgBreakAndParaMark, "SplitPgBreakAndParaMark", enabledOptions, disabledOptions);
    AddOptionName(options.SubFontBySize, "SubFontBySize", enabledOptions, disabledOptions);
    AddOptionName(options.SuppressBottomSpacing, "SuppressBottomSpacing", enabledOptions, disabledOptions);
    AddOptionName(options.SuppressSpBfAfterPgBrk, "SuppressSpBfAfterPgBrk", enabledOptions, disabledOptions);
    AddOptionName(options.SuppressSpacingAtTopOfPage, "SuppressSpacingAtTopOfPage", enabledOptions, disabledOptions);
    AddOptionName(options.SuppressTopSpacing, "SuppressTopSpacing", enabledOptions, disabledOptions);
    AddOptionName(options.SuppressTopSpacingWP, "SuppressTopSpacingWP", enabledOptions, disabledOptions);
    AddOptionName(options.SwapBordersFacingPgs, "SwapBordersFacingPgs", enabledOptions, disabledOptions);
    AddOptionName(options.SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning, "SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning", enabledOptions, disabledOptions);
    AddOptionName(options.TransparentMetafiles, "TransparentMetafiles", enabledOptions, disabledOptions);
    AddOptionName(options.TruncateFontHeightsLikeWP6, "TruncateFontHeightsLikeWP6", enabledOptions, disabledOptions);
    AddOptionName(options.UICompat97To2003, "UICompat97To2003", enabledOptions, disabledOptions);
    AddOptionName(options.UlTrailSpace, "UlTrailSpace", enabledOptions, disabledOptions);
    AddOptionName(options.UnderlineTabInNumList, "UnderlineTabInNumList", enabledOptions, disabledOptions);
    AddOptionName(options.UseAltKinsokuLineBreakRules, "UseAltKinsokuLineBreakRules", enabledOptions, disabledOptions);
    AddOptionName(options.UseAnsiKerningPairs, "UseAnsiKerningPairs", enabledOptions, disabledOptions);
    AddOptionName(options.UseFELayout, "UseFELayout", enabledOptions, disabledOptions);
    AddOptionName(options.UseNormalStyleForList, "UseNormalStyleForList", enabledOptions, disabledOptions);
    AddOptionName(options.UsePrinterMetrics, "UsePrinterMetrics", enabledOptions, disabledOptions);
    AddOptionName(options.UseSingleBorderforContiguousCells, "UseSingleBorderforContiguousCells", enabledOptions, disabledOptions);
    AddOptionName(options.UseWord2002TableStyleRules, "UseWord2002TableStyleRules", enabledOptions, disabledOptions);
    AddOptionName(options.UseWord2010TableStyleRules, "UseWord2010TableStyleRules", enabledOptions, disabledOptions);
    AddOptionName(options.UseWord97LineBreakRules, "UseWord97LineBreakRules", enabledOptions, disabledOptions);
    AddOptionName(options.WPJustification, "WPJustification", enabledOptions, disabledOptions);
    AddOptionName(options.WPSpaceWidth, "WPSpaceWidth", enabledOptions, disabledOptions);
    AddOptionName(options.WrapTrailSpaces, "WrapTrailSpaces", enabledOptions, disabledOptions);
    Console.WriteLine("\tEnabled options:");
    foreach (string optionName in enabledOptions)
        Console.WriteLine($"\t\t{optionName}");
    Console.WriteLine("\tDisabled options:");
    foreach (string optionName in disabledOptions)
        Console.WriteLine($"\t\t{optionName}");
}

private static void AddOptionName(Boolean option, String optionName, IList<string> enabledOptions, IList<string> disabledOptions)
{
    if (option)
        enabledOptions.Add(optionName);
    else
        disabledOptions.Add(optionName);
}
```

### Смотрите также

* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)

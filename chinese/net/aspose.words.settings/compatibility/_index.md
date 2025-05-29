---
title: Compatibility Enum
linktitle: Compatibility
articleTitle: Compatibility
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Settings.Compatibility 枚举以解锁强大的兼容性选项，实现无缝文档处理和增强性能。
type: docs
weight: 6600
url: /zh/net/aspose.words.settings/compatibility/
---
## Compatibility enumeration

指定兼容性选项的名称。

```csharp
public enum Compatibility
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| NoTabHangInd | `0` | 无制表符挂起缩进 |
| NoSpaceRaiseLower | `1` | 无空间 升高 降低 |
| SuppressSpBfAfterPgBrk | `2` | 取消段落分隔符前的空格 |
| WrapTrailSpaces | `3` | 换行尾随空格 |
| PrintColBlack | `4` | 打印列背景 |
| NoColumnBalance | `5` | 无柱平衡 |
| ConvMailMergeEsc | `6` | 转换邮件合并转义符 |
| SuppressTopSpacing | `7` | 抑制顶部间距 |
| UseSingleBorderforContiguousCells | `8` | 对连续单元格使用单边框 |
| TransparentMetafiles | `9` | 透明元文件 |
| ShowBreaksInFrames | `10` | 在框架中显示中断 |
| SwapBordersOddFacingPgs | `11` | 交换奇数页的边框 |
| DoNotLeaveBackslashAlone | `12` | 不要单独留下反斜杠 |
| DoNotExpandOnShiftReturn | `13` | Shift Return 键不展开 |
| UlTrailSpace | `14` | 下划线尾随空格 |
| BalanceSingleByteDoubleByteWidth | `15` | 平衡单字节和双字节宽度 |
| SuppressTopSpacingAtTopOfPage | `16` | 抑制 WordPerfect 中的顶部行距 |
| SpacingInWholePoints | `17` | 整数点间距 |
| PrintBodyTextBeforeHeader | `18` | 在页眉前打印正文 |
| NoLeading | `19` | 无前导 |
| SpaceForUL | `20` | 下划线空格 |
| MWSmallCaps | `21` | MW 小型大写字母 |
| SuppressTopLineSpacingWP | `22` | 抑制 WordPerfect 中的顶部行距 |
| TruncateFontHeightLikeWP6 | `23` | 像 WordPerfect 6 一样截断字体高度 |
| SubFontBySize | `24` | 按大小替换字体 |
| LineWrapLikeWord6 | `25` | 像 Word 一样换行 6 |
| DoNotSuppressParagraphBorder | `26` | 不抑制段落边框 |
| NoExtraLineSpacing | `27` | 无额外行距 |
| SuppressBottomSpacing | `28` | 抑制底部间距 |
| WPSpaceWidth | `29` | WordPerfect 空间宽度 |
| WPJustification | `30` | WordPerfect 对齐 |
| UsePrinterMetrics | `31` | 使用打印机指标 |
| ShapeLayoutLikeWW8 | `32` | 形状布局类似 Word 2000 |
| FootnoteLayoutLikeWW8 | `33` | 脚注布局类似 Word 2000 |
| DoNotUseHtmlParagraphAutoSpacing | `34` | 请勿使用 HTML 段落自动间距 |
| AdjustLineHeightInTable | `35` | 调整表格行高 |
| ForgetLastTabAlignment | `36` | 忘记最后一个标签对齐 |
| AutoSpaceLikeWord95 | `37` | 自动空格类似 Word 95 |
| AlignTableRowByRow | `38` | 按规则对齐表格行 |
| LayoutRawTableWidth | `39` | 布局原始表格宽度 |
| LayoutTableRowsApart | `40` | 布局表格行分开 |
| UseWord97LineBreakRules | `41` | 使用 Word 97 换行规则 |
| DoNotBreakWrappedTables | `42` | 请勿破坏包装的表格 |
| doNotSnapToGridInCell | `43` | 不要对齐单元格中的网格 |
| SelectFldWithFirstOrLastChar | `44` | 选择具有第一个或最后一个字符的字段 |
| ApplyBreakingRules | `45` | 应用违反规则 |
| DoNotWrapTextWithPunct | `46` | 不要用标点符号换行 |
| DoNotUseEastAsianBreakRules | `47` | 请勿使用东亚中断规则 |
| UseWord2002TableStyleRules | `48` | 使用 Word 2002 表格样式规则 |
| GrowAutofit | `49` | 自动适应增长 |
| UseNormalStyleForList | `50` | 使用列表的普通样式 |
| DoNotUseIndentAsNumberingTabStop | `51` | 不使用缩进作为编号制表位 |
| UseAltKinsokuLineBreakRules | `52` | 使用 Alt 避头尾换行规则 |
| AllowSpaceOfSameStyleInTable | `53` | 允许表格中相同样式的空间 |
| DoNotSuppressIndentation | `54` | 不抑制缩进 |
| DoNotAutofitConstrainedTables | `55` | 不自动调整受约束的表格 |
| AutofitToFirstFixedWidthCell | `56` | 自动调整至第一个固定宽度单元格 |
| UnderlineTabInNumList | `57` | 编号列表中的下划线制表符 |
| DisplayHangulFixedWidth | `58` | 显示韩语固定宽度 |
| SplitPgBreakAndParaMark | `59` | 分割分页符和段落标记 |
| DoNotVertAlignCellWithSp | `60` | 不要垂直对齐单元格并留出间距 |
| DoNotBreakConstrainedForcedTable | `61` | 不要破坏受约束的强制表 |
| DoNotVertAlignInTxbx | `62` | 文本框不垂直对齐 |
| UseAnsiKerningPairs | `63` | 使用 ANSI 字距调整对 |
| CachedColBalance | `64` | 缓存列平衡 |
| UseFELayout | `65` | 使用远东布局 |
| UICompat97To2003 | `66` | 从 Word 97 到 Word 2003 的用户界面兼容模式 |
| OverrideTableStyleFontSizeAndJustification | `67` | 覆盖表格样式字体大小和对齐方式 |
| DisableOpenTypeFontFormattingFeatures | `68` | 禁用 OpenType 字体格式化功能 |
| SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning | `69` | 交换内部和外部以进行镜像缩进和相对定位 |
| UseWord2010TableStyleRules | `70` | 使用 Word 2010 表格样式规则 |

## 例子

展示如何针对不同版本的 Microsoft Word 优化文档。

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // 该对象包含每个文档独有的标志的详尽列表
    // 使我们能够实现与旧版本 Microsoft Word 的向后兼容性。
    CompatibilityOptions options = doc.CompatibilityOptions;

    // 打印空白文档的默认设置。
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // 我们可以通过 Microsoft Word 中的“文件”->“选项”->“高级”->“兼容性选项...”访问这些设置。
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // 我们可以使用 OptimizeFor 方法来确保与特定 Microsoft Word 版本的最佳兼容性。
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// 按状态对文档兼容性选项对象中的所有标志进行分组，然后打印每个组。
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

### 也可以看看

* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings/)
* 部件 [Aspose.Words](../../)

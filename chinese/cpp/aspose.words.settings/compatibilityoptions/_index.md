---
title: "Aspose::Words::Settings::CompatibilityOptions 类"
linktitle: "CompatibilityOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::CompatibilityOptions 类。包含兼容性选项（即用户在 Microsoft Word 的选项对话框的兼容性选项卡中输入的首选项）。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.settings/compatibilityoptions/
---
## CompatibilityOptions class


包含兼容性选项（即在 Microsoft Word 的 **Options** 对话框的 **Compatibility** 选项卡中输入的用户首选项）。欲了解更多，请访问 [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/) 文档文章。

```cpp
class CompatibilityOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_AdjustLineHeightInTable](./get_adjustlineheightintable/)() | 向表格单元格中的线添加 [Document](../../aspose.words/document/) 网格线间距。 |
| [get_AlignTablesRowByRow](./get_aligntablesrowbyrow/)() | 独立对齐表格行。 |
| [get_AllowSpaceOfSameStyleInTable](./get_allowspaceofsamestyleintable/)() | 允许在 [Tables](../../aspose.words.tables/) 中的段落进行上下文间距。 |
| [get_ApplyBreakingRules](./get_applybreakingrules/)() | 使用传统的埃塞俄比亚语和阿姆哈拉语换行规则。 |
| [get_AutofitToFirstFixedWidthCell](./get_autofittofirstfixedwidthcell/)() | 允许表格列超过其组成单元格的首选宽度。 |
| [get_AutoSpaceLikeWord95](./get_autospacelikeword95/)() | 模拟 Word 95 全角字符间距。 |
| [get_BalanceSingleByteDoubleByteWidth](./get_balancesinglebytedoublebytewidth/)() | 平衡单字节和双字节字符。 |
| [get_CachedColBalance](./get_cachedcolbalance/)() | 使用缓存的 [Paragraph](../../aspose.words/paragraph/) 信息进行列平衡。 |
| [get_ConvMailMergeEsc](./get_convmailmergeesc/)() | 将反斜杠引号分隔符视为两个引号。 |
| [get_DisableOpenTypeFontFormattingFeatures](./get_disableopentypefontformattingfeatures/)() | 指定禁用 OpenType 字体格式化功能。 |
| [get_DisplayHangulFixedWidth](./get_displayhangulfixedwidth/)() | 始终对韩文字符使用固定宽度。 |
| [get_DoNotAutofitConstrainedTables](./get_donotautofitconstrainedtables/)() | 不要自动调整 [Tables](../../aspose.words.tables/) 以适应环绕对象旁边。 |
| [get_DoNotBreakConstrainedForcedTable](./get_donotbreakconstrainedforcedtable/)() | 不要在浮动的 [Tables](../../aspose.words.tables/) 周围断开表行。 |
| [get_DoNotBreakWrappedTables](./get_donotbreakwrappedtables/)() | 不允许浮动的 [Tables](../../aspose.words.tables/) 跨页断开。 |
| [get_DoNotExpandShiftReturn](./get_donotexpandshiftreturn/)() | 不要两端对齐以软换行结尾的行。 |
| [get_DoNotLeaveBackslashAlone](./get_donotleavebackslashalone/)() | 输入时将反斜杠转换为日元符号。 |
| [get_DoNotSnapToGridInCell](./get_donotsnaptogridincell/)() | 不要在包含对象的表格单元格中对齐到 [Document](../../aspose.words/document/) 网格。 |
| [get_DoNotSuppressIndentation](./get_donotsuppressindentation/)() | 计算 [Paragraph](../../aspose.words/paragraph/) 缩进时不要忽略浮动对象。 |
| [get_DoNotSuppressParagraphBorders](./get_donotsuppressparagraphborders/)() | 不要在框架旁抑制 [Paragraph](../../aspose.words/paragraph/) 边框。 |
| [get_DoNotUseEastAsianBreakRules](./get_donotuseeastasianbreakrules/)() | 使用 [Document](../../aspose.words/document/) 网格时不要压缩可压缩字符。 |
| [get_DoNotUseHTMLParagraphAutoSpacing](./get_donotusehtmlparagraphautospacing/)() | 对 HTML 自动设置使用固定的 [Paragraph](../../aspose.words/paragraph/) 间距。 |
| [get_DoNotUseIndentAsNumberingTabStop](./get_donotuseindentasnumberingtabstop/)() | 在编号后创建制表位时忽略悬挂缩进。 |
| [get_DoNotVertAlignCellWithSp](./get_donotvertaligncellwithsp/)() | 不要垂直对齐包含浮动对象的单元格。 |
| [get_DoNotVertAlignInTxbx](./get_donotvertalignintxbx/)() | 忽略文本框中的垂直对齐。 |
| [get_DoNotWrapTextWithPunct](./get_donotwraptextwithpunct/)() | 不要在字符网格中允许悬挂标点。 |
| [get_FootnoteLayoutLikeWW8](./get_footnotelayoutlikeww8/)() | 模拟 Word 6.x/95/97 脚注位置。 |
| [get_ForgetLastTabAlignment](./get_forgetlasttabalignment/)() | 如果 [Paragraph](../../aspose.words/paragraph/) 未左对齐，则在对齐时忽略最后一个制表位的宽度。 |
| [get_GrowAutofit](./get_growautofit/)() | 允许 [Tables](../../aspose.words.tables/) 自动适应页面边距。 |
| [get_LayoutRawTableWidth](./get_layoutrawtablewidth/)() | 在决定表格是否应环绕浮动对象时，忽略表格前的空格。 |
| [get_LayoutTableRowsApart](./get_layouttablerowsapart/)() | 允许表格行独立换行包裹 [Inline](../../aspose.words/inline/) 对象。 |
| [get_LineWrapLikeWord6](./get_linewraplikeword6/)() | 模拟 Word 6.0 对东亚文字的换行。 |
| [get_MWSmallCaps](./get_mwsmallcaps/)() | 模拟 Word 5.x 在 Macintosh 上的小型大写字母格式。 |
| [get_NoColumnBalance](./get_nocolumnbalance/)() | 不要在 [Section](../../aspose.words/section/) 中平衡文本列。 |
| [get_NoExtraLineSpacing](./get_noextralinespacing/)() | 不要在具有精确行高的行上居中内容。 |
| [get_NoLeading](./get_noleading/)() | 不要在文本行之间添加行距。 |
| [get_NoSpaceRaiseLower](./get_nospaceraiselower/)() | 不要为升高/降低的文本增加行高。 |
| [get_NoTabHangInd](./get_notabhangind/)() | 不要为悬挂缩进创建自定义制表位。 |
| [get_OverrideTableStyleFontSizeAndJustification](./get_overridetablestylefontsizeandjustification/)() | 指定文档样式层次结构的评估方式。 |
| [get_PrintBodyTextBeforeHeader](./get_printbodytextbeforeheader/)() | 在页眉/页脚内容之前打印 [Body](../../aspose.words/body/) 文本。 |
| [get_PrintColBlack](./get_printcolblack/)() | 以黑白方式打印颜色且不使用抖动。 |
| [get_SelectFldWithFirstOrLastChar](./get_selectfldwithfirstorlastchar/)() | 当选中首字符或尾字符时选择字段。 |
| [get_ShapeLayoutLikeWW8](./get_shapelayoutlikeww8/)() | 模拟 Word 97 环绕浮动对象的文本换行。 |
| [get_ShowBreaksInFrames](./get_showbreaksinframes/)() | 显示框架中存在的页面/列分隔符。 |
| [get_SpaceForUL](./get_spaceforul/)() | 为带下划线的东亚文字在基线下方添加额外空间。 |
| [get_SpacingInWholePoints](./get_spacinginwholepoints/)() | 仅按整数点数扩展/压缩文本。 |
| [get_SplitPgBreakAndParaMark](./get_splitpgbreakandparamark/)() | 在分页符后始终将 [Paragraph](../../aspose.words/paragraph/) 标记移动到页面。 |
| [get_SubFontBySize](./get_subfontbysize/)() | 在 [Font](../../aspose.words/font/) 替换期间提高 [Font](../../aspose.words/font/) 大小的优先级。 |
| [get_SuppressBottomSpacing](./get_suppressbottomspacing/)() | 忽略页面最后一行的精确行高。 |
| [get_SuppressSpacingAtTopOfPage](./get_suppressspacingattopofpage/)() | 忽略页面第一行的最小行高。 |
| [get_SuppressSpBfAfterPgBrk](./get_suppressspbfafterpgbrk/)() | 在分页符后的第一行不要使用前置空格。 |
| [get_SuppressTopSpacing](./get_suppresstopspacing/)() | 忽略页面第一行的最小行高和精确行高。 |
| [get_SuppressTopSpacingWP](./get_suppresstopspacingwp/)() | 模拟 WordPerfect 5.x 行间距。 |
| [get_SwapBordersFacingPgs](./get_swapbordersfacingpgs/)() | 在奇数页上交换 [Paragraph](../../aspose.words/paragraph/) 边框。 |
| [get_SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning](./get_swapinsideandoutsideformirrorindentsandrelativepositioning/)() | 指定在镜像缩进和相对定位时交换内部和外部。 |
| [get_TransparentMetafiles](./get_transparentmetafiles/)() | 指定不清除元文件图片后面的区域。 |
| [get_TruncateFontHeightsLikeWP6](./get_truncatefontheightslikewp6/)() | 模拟 WordPerfect 6.x [Font](../../aspose.words/font/) 高度计算。 |
| [get_UICompat97To2003](./get_uicompat97to2003/)() | 设置为 True 可禁用与 Word97-2003 不兼容的 UI 功能。默认值为 **false**。 |
| [get_UlTrailSpace](./get_ultrailspace/)() | 为所有尾随空格添加下划线。 |
| [get_UnderlineTabInNumList](./get_underlinetabinnumlist/)() | 在编号后面的字符添加下划线。 |
| [get_UseAltKinsokuLineBreakRules](./get_usealtkinsokulinebreakrules/)() | 使用备用的东亚换行规则集。 |
| [get_UseAnsiKerningPairs](./get_useansikerningpairs/)() | 使用来自 [Fonts](../../aspose.words.fonts/) 的 ANSI 字距对。 |
| [get_UseFELayout](./get_usefelayout/)() | 不要绕过东亚/复杂脚本 [Layout](../../aspose.words.layout/) 代码。 |
| [get_UseNormalStyleForList](./get_usenormalstyleforlist/)() | 不要自动将列表 [Paragraph](../../aspose.words/paragraph/)[Style](../../aspose.words/style/) 应用于项目符号/编号文本。 |
| [get_UsePrinterMetrics](./get_useprintermetrics/)() | 使用打印机度量来显示文档。 |
| [get_UseSingleBorderforContiguousCells](./get_usesingleborderforcontiguouscells/)() | 对表格 [Border](../../aspose.words/border/) 冲突使用简化规则。 |
| [get_UseWord2002TableStyleRules](./get_useword2002tablestylerules/)() | 模拟 Word 2002 表格 [Style](../../aspose.words/style/) 规则。 |
| [get_UseWord2010TableStyleRules](./get_useword2010tablestylerules/)() | 指定使用 Word2010 表格样式规则。 |
| [get_UseWord97LineBreakRules](./get_useword97linebreakrules/)() | 模拟 Word 97 东亚换行。 |
| [get_WPJustification](./get_wpjustification/)() | 模拟 WordPerfect 6.x [Paragraph](../../aspose.words/paragraph/) 对齐方式。 |
| [get_WPSpaceWidth](./get_wpspacewidth/)() | 指定是否将空格的宽度设置为 WordPerfect 5.x 中的方式。 |
| [get_WrapTrailSpaces](./get_wraptrailspaces/)() | 对尾随空格进行换行。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OptimizeFor](./optimizefor/)(Aspose::Words::Settings::MsWordVersion) | 允许将文档内容以及默认的 Aspose.Words 行为优化到特定的 MS Word 版本。使用此方法可防止 MS Word 在加载文档时显示 "Compatibility mode" 功能区。（注意，您可能还需要将 [Compliance](../../aspose.words.saving/ooxmlsaveoptions/get_compliance/) 属性设置为 [Iso29500_2008_Transitional](../../aspose.words.saving/ooxmlcompliance/) 或更高版本。） |
| [set_AdjustLineHeightInTable](./set_adjustlineheightintable/)(bool) | 向表格单元格中的线添加 [Document](../../aspose.words/document/) 网格线间距。 |
| [set_AlignTablesRowByRow](./set_aligntablesrowbyrow/)(bool) | 独立对齐表格行。 |
| [set_AllowSpaceOfSameStyleInTable](./set_allowspaceofsamestyleintable/)(bool) | 允许在 [Tables](../../aspose.words.tables/) 中的段落进行上下文间距。 |
| [set_ApplyBreakingRules](./set_applybreakingrules/)(bool) | 使用传统的埃塞俄比亚语和阿姆哈拉语换行规则。 |
| [set_AutofitToFirstFixedWidthCell](./set_autofittofirstfixedwidthcell/)(bool) | 允许表格列超过其组成单元格的首选宽度。 |
| [set_AutoSpaceLikeWord95](./set_autospacelikeword95/)(bool) | 模拟 Word 95 全角字符间距。 |
| [set_BalanceSingleByteDoubleByteWidth](./set_balancesinglebytedoublebytewidth/)(bool) | 平衡单字节和双字节字符。 |
| [set_CachedColBalance](./set_cachedcolbalance/)(bool) | 使用缓存的 [Paragraph](../../aspose.words/paragraph/) 信息进行列平衡。 |
| [set_ConvMailMergeEsc](./set_convmailmergeesc/)(bool) | 将反斜杠引号分隔符视为两个引号。 |
| [set_DisableOpenTypeFontFormattingFeatures](./set_disableopentypefontformattingfeatures/)(bool) | 指定禁用 OpenType 字体格式化功能。 |
| [set_DisplayHangulFixedWidth](./set_displayhangulfixedwidth/)(bool) | 始终对韩文字符使用固定宽度。 |
| [set_DoNotAutofitConstrainedTables](./set_donotautofitconstrainedtables/)(bool) | 不要自动调整 [Tables](../../aspose.words.tables/) 以适应环绕对象旁边。 |
| [set_DoNotBreakConstrainedForcedTable](./set_donotbreakconstrainedforcedtable/)(bool) | 不要在浮动的 [Tables](../../aspose.words.tables/) 周围断开表行。 |
| [set_DoNotBreakWrappedTables](./set_donotbreakwrappedtables/)(bool) | 不允许浮动的 [Tables](../../aspose.words.tables/) 跨页断开。 |
| [set_DoNotExpandShiftReturn](./set_donotexpandshiftreturn/)(bool) | 不要两端对齐以软换行结尾的行。 |
| [set_DoNotLeaveBackslashAlone](./set_donotleavebackslashalone/)(bool) | 输入时将反斜杠转换为日元符号。 |
| [set_DoNotSnapToGridInCell](./set_donotsnaptogridincell/)(bool) | 不要在包含对象的表格单元格中对齐到 [Document](../../aspose.words/document/) 网格。 |
| [set_DoNotSuppressIndentation](./set_donotsuppressindentation/)(bool) | 计算 [Paragraph](../../aspose.words/paragraph/) 缩进时不要忽略浮动对象。 |
| [set_DoNotSuppressParagraphBorders](./set_donotsuppressparagraphborders/)(bool) | 不要在框架旁抑制 [Paragraph](../../aspose.words/paragraph/) 边框。 |
| [set_DoNotUseEastAsianBreakRules](./set_donotuseeastasianbreakrules/)(bool) | 使用 [Document](../../aspose.words/document/) 网格时不要压缩可压缩字符。 |
| [set_DoNotUseHTMLParagraphAutoSpacing](./set_donotusehtmlparagraphautospacing/)(bool) | 对 HTML 自动设置使用固定的 [Paragraph](../../aspose.words/paragraph/) 间距。 |
| [set_DoNotUseIndentAsNumberingTabStop](./set_donotuseindentasnumberingtabstop/)(bool) | 在编号后创建制表位时忽略悬挂缩进。 |
| [set_DoNotVertAlignCellWithSp](./set_donotvertaligncellwithsp/)(bool) | 不要垂直对齐包含浮动对象的单元格。 |
| [set_DoNotVertAlignInTxbx](./set_donotvertalignintxbx/)(bool) | 忽略文本框中的垂直对齐。 |
| [set_DoNotWrapTextWithPunct](./set_donotwraptextwithpunct/)(bool) | 不要在字符网格中允许悬挂标点。 |
| [set_FootnoteLayoutLikeWW8](./set_footnotelayoutlikeww8/)(bool) | 模拟 Word 6.x/95/97 脚注位置。 |
| [set_ForgetLastTabAlignment](./set_forgetlasttabalignment/)(bool) | 如果 [Paragraph](../../aspose.words/paragraph/) 未左对齐，则在对齐时忽略最后一个制表位的宽度。 |
| [set_GrowAutofit](./set_growautofit/)(bool) | 允许 [Tables](../../aspose.words.tables/) 自动适应页面边距。 |
| [set_LayoutRawTableWidth](./set_layoutrawtablewidth/)(bool) | 在决定表格是否应环绕浮动对象时，忽略表格前的空格。 |
| [set_LayoutTableRowsApart](./set_layouttablerowsapart/)(bool) | 允许表格行独立换行包裹 [Inline](../../aspose.words/inline/) 对象。 |
| [set_LineWrapLikeWord6](./set_linewraplikeword6/)(bool) | 模拟 Word 6.0 对东亚文字的换行。 |
| [set_MWSmallCaps](./set_mwsmallcaps/)(bool) | 模拟 Word 5.x 在 Macintosh 上的小型大写字母格式。 |
| [set_NoColumnBalance](./set_nocolumnbalance/)(bool) | 不要在 [Section](../../aspose.words/section/) 中平衡文本列。 |
| [set_NoExtraLineSpacing](./set_noextralinespacing/)(bool) | 不要在具有精确行高的行上居中内容。 |
| [set_NoLeading](./set_noleading/)(bool) | 不要在文本行之间添加行距。 |
| [set_NoSpaceRaiseLower](./set_nospaceraiselower/)(bool) | 不要为升高/降低的文本增加行高。 |
| [set_NoTabHangInd](./set_notabhangind/)(bool) | 不要为悬挂缩进创建自定义制表位。 |
| [set_OverrideTableStyleFontSizeAndJustification](./set_overridetablestylefontsizeandjustification/)(bool) | 指定文档样式层次结构的评估方式。 |
| [set_PrintBodyTextBeforeHeader](./set_printbodytextbeforeheader/)(bool) | 在页眉/页脚内容之前打印 [Body](../../aspose.words/body/) 文本。 |
| [set_PrintColBlack](./set_printcolblack/)(bool) | 以黑白方式打印颜色且不使用抖动。 |
| [set_SelectFldWithFirstOrLastChar](./set_selectfldwithfirstorlastchar/)(bool) | 当选中首字符或尾字符时选择字段。 |
| [set_ShapeLayoutLikeWW8](./set_shapelayoutlikeww8/)(bool) | 模拟 Word 97 环绕浮动对象的文本换行。 |
| [set_ShowBreaksInFrames](./set_showbreaksinframes/)(bool) | 显示框架中存在的页面/列分隔符。 |
| [set_SpaceForUL](./set_spaceforul/)(bool) | 为带下划线的东亚文字在基线下方添加额外空间。 |
| [set_SpacingInWholePoints](./set_spacinginwholepoints/)(bool) | 仅按整数点数扩展/压缩文本。 |
| [set_SplitPgBreakAndParaMark](./set_splitpgbreakandparamark/)(bool) | 在分页符后始终将 [Paragraph](../../aspose.words/paragraph/) 标记移动到页面。 |
| [set_SubFontBySize](./set_subfontbysize/)(bool) | 在 [Font](../../aspose.words/font/) 替换期间提高 [Font](../../aspose.words/font/) 大小的优先级。 |
| [set_SuppressBottomSpacing](./set_suppressbottomspacing/)(bool) | 忽略页面最后一行的精确行高。 |
| [set_SuppressSpacingAtTopOfPage](./set_suppressspacingattopofpage/)(bool) | 忽略页面第一行的最小行高。 |
| [set_SuppressSpBfAfterPgBrk](./set_suppressspbfafterpgbrk/)(bool) | 在分页符后的第一行不要使用前置空格。 |
| [set_SuppressTopSpacing](./set_suppresstopspacing/)(bool) | 忽略页面第一行的最小行高和精确行高。 |
| [set_SuppressTopSpacingWP](./set_suppresstopspacingwp/)(bool) | 模拟 WordPerfect 5.x 行间距。 |
| [set_SwapBordersFacingPgs](./set_swapbordersfacingpgs/)(bool) | 在奇数页上交换 [Paragraph](../../aspose.words/paragraph/) 边框。 |
| [set_SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning](./set_swapinsideandoutsideformirrorindentsandrelativepositioning/)(bool) | 指定在镜像缩进和相对定位时交换内部和外部。 |
| [set_TransparentMetafiles](./set_transparentmetafiles/)(bool) | 指定不清除元文件图片后面的区域。 |
| [set_TruncateFontHeightsLikeWP6](./set_truncatefontheightslikewp6/)(bool) | 模拟 WordPerfect 6.x [Font](../../aspose.words/font/) 高度计算。 |
| [set_UICompat97To2003](./set_uicompat97to2003/)(bool) | 设置为 True 可禁用与 Word97-2003 不兼容的 UI 功能。默认值为 **false**。 |
| [set_UlTrailSpace](./set_ultrailspace/)(bool) | 为所有尾随空格添加下划线。 |
| [set_UnderlineTabInNumList](./set_underlinetabinnumlist/)(bool) | 在编号后面的字符添加下划线。 |
| [set_UseAltKinsokuLineBreakRules](./set_usealtkinsokulinebreakrules/)(bool) | 使用备用的东亚换行规则集。 |
| [set_UseAnsiKerningPairs](./set_useansikerningpairs/)(bool) | 使用来自 [Fonts](../../aspose.words.fonts/) 的 ANSI 字距对。 |
| [set_UseFELayout](./set_usefelayout/)(bool) | 不要绕过东亚/复杂脚本 [Layout](../../aspose.words.layout/) 代码。 |
| [set_UseNormalStyleForList](./set_usenormalstyleforlist/)(bool) | 不要自动将列表 [Paragraph](../../aspose.words/paragraph/)[Style](../../aspose.words/style/) 应用于项目符号/编号文本。 |
| [set_UsePrinterMetrics](./set_useprintermetrics/)(bool) | 使用打印机度量来显示文档。 |
| [set_UseSingleBorderforContiguousCells](./set_usesingleborderforcontiguouscells/)(bool) | 对表格 [Border](../../aspose.words/border/) 冲突使用简化规则。 |
| [set_UseWord2002TableStyleRules](./set_useword2002tablestylerules/)(bool) | 模拟 Word 2002 表格 [Style](../../aspose.words/style/) 规则。 |
| [set_UseWord2010TableStyleRules](./set_useword2010tablestylerules/)(bool) | 指定使用 Word2010 表格样式规则。 |
| [set_UseWord97LineBreakRules](./set_useword97linebreakrules/)(bool) | 模拟 Word 97 东亚换行。 |
| [set_WPJustification](./set_wpjustification/)(bool) | 模拟 WordPerfect 6.x [Paragraph](../../aspose.words/paragraph/) 对齐方式。 |
| [set_WPSpaceWidth](./set_wpspacewidth/)(bool) | 指定是否将空格的宽度设置为 WordPerfect 5.x 中的方式。 |
| [set_WrapTrailSpaces](./set_wraptrailspaces/)(bool) | 对尾随空格进行换行。 |
| static [Type](./type/)() |  |

## 示例



展示如何为已保存的文档设置 OOXML 合规规范以遵循。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 如果我们将兼容性选项配置为符合 Microsoft Word 2003，
// 插入图像将使用 VML 定义其形状。
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Vml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());

// "ISO/IEC 29500:2008" OOXML 标准不支持 VML 形状。
// 如果我们将 SaveOptions 对象的 \"Compliance\" 属性设置为 \"OoxmlCompliance.Iso29500_2008_Strict\",
// 任何在传递此对象时保存的文档都必须遵循该标准。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docx);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// 我们保存的文档使用 DML 定义形状，以符合 \"ISO/IEC 29500:2008\" OOXML 标准。
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());
```


展示如何垂直对齐文本框的文本内容。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// 将 "VerticalAnchor" 属性设置为 "TextBoxAnchor.Top" 以
// 使此文本框中的文本与形状的顶部对齐。
// 将 "VerticalAnchor" 属性设置为 "TextBoxAnchor.Middle" 以
// 使此文本框中的文本居中于形状。
// 将 "VerticalAnchor" 属性设置为 "TextBoxAnchor.Bottom" 以
// 使此文本框中的文本与形状的底部对齐。
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// 从 Microsoft Word 2007 起，文本框内文本的垂直对齐功能可用。
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## 另见

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)

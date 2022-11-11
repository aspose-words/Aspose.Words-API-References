---
title: CompatibilityOptions
second_title: Aspose.Words for Java API Reference
description: 包含兼容性选项，即在 Microsoft Word 中选项对话框的兼容性选项卡上输入的用户首选项。
type: docs
weight: 86
url: /zh/java/com.aspose.words/compatibilityoptions/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Cloneable
```
public class CompatibilityOptions implements Cloneable
```

包含兼容性选项（即，在**Compatibility**的选项卡**Options**Microsoft Word 中的对话框）。

要了解更多信息，请访问**Detect File Format and Check Format Compatibility**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAdjustLineHeightInTable()](#getAdjustLineHeightInTable--) | 将文档网格线间距添加到表格单元格中的线。 |
| [getAlignTablesRowByRow()](#getAlignTablesRowByRow--) | 独立对齐表格行。 |
| [getAllowSpaceOfSameStyleInTable()](#getAllowSpaceOfSameStyleInTable--) | 允许表格中段落的上下文间距。 |
| [getApplyBreakingRules()](#getApplyBreakingRules--) | 使用传统的埃塞俄比亚语和阿姆哈拉语换行规则。 |
| [getAutoSpaceLikeWord95()](#getAutoSpaceLikeWord95--) | 模拟 Word 95 全角字符间距。 |
| [getAutofitToFirstFixedWidthCell()](#getAutofitToFirstFixedWidthCell--) | 允许表格列超过组成单元格的首选宽度。 |
| [getBalanceSingleByteDoubleByteWidth()](#getBalanceSingleByteDoubleByteWidth--) | 平衡单字节和双字节字符。 |
| [getCachedColBalance()](#getCachedColBalance--) | 使用缓存的段落信息进行列平衡。 |
| [get班级()](#get班级--) |  |
| [getConvMailMergeEsc()](#getConvMailMergeEsc--) | 将反斜杠引号分隔符视为两个引号。 |
| [getDisableOpen类型FontFormattingFeatures()](#getDisableOpen类型FontFormattingFeatures--) |  |
| [getDisplayHangulFixedWidth()](#getDisplayHangulFixedWidth--) | 始终为韩文字符使用固定宽度。 |
| [getDoNotAutofitConstrainedTables()](#getDoNotAutofitConstrainedTables--) | 不要自动调整表格以适合包裹的对象。 |
| [getDoNotBreakConstrainedForcedTable()](#getDoNotBreakConstrainedForcedTable--) | 不要打破浮动表周围的表行。 |
| [getDoNotBreakWrappedTables()](#getDoNotBreakWrappedTables--) | 不允许浮动表格跨越页面。 |
| [getDoNotExpandShiftReturn()](#getDoNotExpandShiftReturn--) | 不要证明以软换行符结尾的行。 |
| [getDoNotLeaveBackslashAlone()](#getDoNotLeaveBackslashAlone--) | 输入时将反斜杠转换为日元符号。 |
| [getDoNotSnapToGridInCell()](#getDoNotSnapToGridInCell--) | 不要在包含对象的表格单元格中对齐文档网格。 |
| [getDoNotSuppressIndentation()](#getDoNotSuppressIndentation--) | 计算段落缩进时不要忽略浮动对象。 |
| [getDoNotSuppressParagraphBorders()](#getDoNotSuppressParagraphBorders--) | 不要抑制框架旁边的段落边框。 |
| [getDoNotUseEastAsianBreakRules()](#getDoNotUseEastAsianBreakRules--) | 使用文档网格时不要压缩可压缩字符。 |
| [getDoNotUseHTMLParagraphAutoSpacing()](#getDoNotUseHTMLParagraphAutoSpacing--) | 为 HTML 自动设置使用固定段落间距。 |
| [getDoNotUseIndentAsNumberingTabStop()](#getDoNotUseIndentAsNumberingTabStop--) | 编号后创建制表位时忽略悬挂缩进。 |
| [getDoNotVertAlignCellWithSp()](#getDoNotVertAlignCellWithSp--) | 不要垂直对齐包含浮动对象的单元格。 |
| [getDoNotVertAlignInTxbx()](#getDoNotVertAlignInTxbx--) | 忽略文本框中的垂直对齐。 |
| [getDoNotWrapTextWithPunct()](#getDoNotWrapTextWithPunct--) | 不允许使用字符网格悬挂标点。 |
| [getFootnoteLayoutLikeWW8()](#getFootnoteLayoutLikeWW8--) | 模拟 Word 6.x/95/97 脚注放置。 |
| [getForgetLastTabAlignment()](#getForgetLastTabAlignment--) | 如果段落未左对齐，则在对齐段落时忽略最后一个制表位的宽度。 |
| [getGrowAutofit()](#getGrowAutofit--) | 允许表格自动适应页边距。 |
| [getLayoutRawTableWidth()](#getLayoutRawTableWidth--) | 在决定表是否应该包裹浮动对象时忽略表前的空格。 |
| [getLayoutTableRowsApart()](#getLayoutTableRowsApart--) | 允许表格行独立包装内联对象。 |
| [getLineWrapLikeWord6()](#getLineWrapLikeWord6--) | 为东亚文本模拟 Word 6.0 换行。 |
| [getMWSmallCaps()](#getMWSmallCaps--) | 模拟 Macintosh Small Caps 格式的 Word 5.x。 |
| [getNoColumnBalance()](#getNoColumnBalance--) | 不要平衡节内的文本列。 |
| [getNoExtraLineSpacing()](#getNoExtraLineSpacing--) | 不要在具有精确行高的行上居中内容。 |
| [getNoLeading()](#getNoLeading--) | 不要在文本行之间添加前导。 |
| [getNoSpaceRaiseLower()](#getNoSpaceRaiseLower--) | 不要增加凸起/降低文本的行高。 |
| [getNoTabHangInd()](#getNoTabHangInd--) | 不要为悬挂缩进创建自定义制表位。 |
| [getOverrideTableStyleFontSizeAndJustification()](#getOverrideTableStyleFontSizeAndJustification--) | 指定如何评估文档的样式层次结构。 |
| [getPrintBodyTextBeforeHeader()](#getPrintBodyTextBeforeHeader--) | 在页眉/页脚内容之前打印正文文本。 |
| [getPrintColBlack()](#getPrintColBlack--) | 将颜色打印为黑色和白色，无需抖动。 |
| [getSelectFldWithFirstOrLastChar()](#getSelectFldWithFirstOrLastChar--) | 选择第一个或最后一个字符时选择字段。 |
| [getShapeLayoutLikeWW8()](#getShapeLayoutLikeWW8--) | 模拟环绕浮动对象的 Word 97 文本。 |
| [getShowBreaksInFrames()](#getShowBreaksInFrames--) | 显示帧中存在的分页符/分栏符。 |
| [getSpaceForUL()](#getSpaceForUL--) | 在基线下方为带下划线的东亚文本添加额外的空间。 |
| [getSpacingInWholePoints()](#getSpacingInWholePoints--) | 仅按整点扩展/压缩文本。 |
| [getSplitPgBreakAndParaMark()](#getSplitPgBreakAndParaMark--) | 总是在分页后将段落标记移动到页面。 |
| [getSubFontBySize()](#getSubFontBySize--) | 在字体替换期间增加字体大小的优先级。 |
| [getSuppressBottomSpacing()](#getSuppressBottomSpacing--) | 忽略页面上最后一行的确切行高。 |
| [getSuppressSpBfAfterPgBrk()](#getSuppressSpBfAfterPgBrk--) | 不要在分页后的第一行之前使用空格。 |
| [getSuppressSpacingAtTopOfPage()](#getSuppressSpacingAtTopOfPage--) | 忽略页面上第一行的最小行高。 |
| [getSuppressTopSpacing()](#getSuppressTopSpacing--) | 忽略页面上第一行的最小和精确行高。 |
| [getSuppressTopSpacingWP()](#getSuppressTopSpacingWP--) | 模拟 WordPerfect 5.x 行间距。 |
| [getSwapBordersFacingPgs()](#getSwapBordersFacingPgs--) | 在奇数页上交换段落边框。 |
| [getSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning()](#getSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning--) |  |
| [getTransparentMetafiles()](#getTransparentMetafiles--) | 指定不空白图元文件图片后面的区域。 |
| [getTruncateFontHeightsLikeWP6()](#getTruncateFontHeightsLikeWP6--) | 模拟 WordPerfect 6.x 字体高度计算。 |
| [getUICompat97To2003()](#getUICompat97To2003--) | **True**禁用与 Word97-2003 不兼容的 UI 功能。 |
| [getUlTrailSpace()](#getUlTrailSpace--) | 在所有尾随空格下划线。 |
| [getUnderlineTabInNumList()](#getUnderlineTabInNumList--) | 在编号后的字符后加下划线。 |
| [getUseAltKinsokuLineBreakRules()](#getUseAltKinsokuLineBreakRules--) | 使用另一种东亚断线规则。 |
| [getUseAnsiKerningPairs()](#getUseAnsiKerningPairs--) | 使用字体中的 ANSI Kerning Pairs。 |
| [getUseFELayout()](#getUseFELayout--) | 不要绕过东亚/复杂脚本布局代码。 |
| [getUseNormalStyleForList()](#getUseNormalStyleForList--) | 不要自动将列表段落样式应用于项目符号/编号文本。 |
| [getUsePrinterMetrics()](#getUsePrinterMetrics--) | 使用打印机度量来显示文档。 |
| [getUseSingleBorderforContiguousCells()](#getUseSingleBorderforContiguousCells--) | 对表格边界冲突使用简化规则。 |
| [getUseWord2002TableStyleRules()](#getUseWord2002TableStyleRules--) | 模拟 Word 2002 表格样式规则。 |
| [getUseWord2010TableStyleRules()](#getUseWord2010TableStyleRules--) |  |
| [getUseWord97LineBreakRules()](#getUseWord97LineBreakRules--) | 模拟 Word 97 东亚换行。 |
| [getWPJustification()](#getWPJustification--) | 模拟 WordPerfect 6.x 段落对齐。 |
| [getWPSpaceWidth()](#getWPSpaceWidth--) | 指定是否像在 WordPerfect 5.x 中那样设置空格的宽度。 |
| [getWrapTrailSpaces()](#getWrapTrailSpaces--) | 换行尾随空格。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [optimizeFor(int version)](#optimizeFor-int-) |  |
| [setAdjustLineHeightInTable(boolean value)](#setAdjustLineHeightInTable-boolean-) | 将文档网格线间距添加到表格单元格中的线。 |
| [setAlignTablesRowByRow(boolean value)](#setAlignTablesRowByRow-boolean-) | 独立对齐表格行。 |
| [setAllowSpaceOfSameStyleInTable(boolean value)](#setAllowSpaceOfSameStyleInTable-boolean-) | 允许表格中段落的上下文间距。 |
| [setApplyBreakingRules(boolean value)](#setApplyBreakingRules-boolean-) | 使用传统的埃塞俄比亚语和阿姆哈拉语换行规则。 |
| [setAutoSpaceLikeWord95(boolean value)](#setAutoSpaceLikeWord95-boolean-) | 模拟 Word 95 全角字符间距。 |
| [setAutofitToFirstFixedWidthCell(boolean value)](#setAutofitToFirstFixedWidthCell-boolean-) | 允许表格列超过组成单元格的首选宽度。 |
| [setBalanceSingleByteDoubleByteWidth(boolean value)](#setBalanceSingleByteDoubleByteWidth-boolean-) | 平衡单字节和双字节字符。 |
| [setCachedColBalance(boolean value)](#setCachedColBalance-boolean-) | 使用缓存的段落信息进行列平衡。 |
| [setConvMailMergeEsc(boolean value)](#setConvMailMergeEsc-boolean-) | 将反斜杠引号分隔符视为两个引号。 |
| [setDisableOpen类型FontFormattingFeatures(boolean value)](#setDisableOpen类型FontFormattingFeatures-boolean-) |  |
| [setDisplayHangulFixedWidth(boolean value)](#setDisplayHangulFixedWidth-boolean-) | 始终为韩文字符使用固定宽度。 |
| [setDoNotAutofitConstrainedTables(boolean value)](#setDoNotAutofitConstrainedTables-boolean-) | 不要自动调整表格以适合包裹的对象。 |
| [setDoNotBreakConstrainedForcedTable(boolean value)](#setDoNotBreakConstrainedForcedTable-boolean-) | 不要打破浮动表周围的表行。 |
| [setDoNotBreakWrappedTables(boolean value)](#setDoNotBreakWrappedTables-boolean-) | 不允许浮动表格跨越页面。 |
| [setDoNotExpandShiftReturn(boolean value)](#setDoNotExpandShiftReturn-boolean-) | 不要证明以软换行符结尾的行。 |
| [setDoNotLeaveBackslashAlone(boolean value)](#setDoNotLeaveBackslashAlone-boolean-) | 输入时将反斜杠转换为日元符号。 |
| [setDoNotSnapToGridInCell(boolean value)](#setDoNotSnapToGridInCell-boolean-) | 不要在包含对象的表格单元格中对齐文档网格。 |
| [setDoNotSuppressIndentation(boolean value)](#setDoNotSuppressIndentation-boolean-) | 计算段落缩进时不要忽略浮动对象。 |
| [setDoNotSuppressParagraphBorders(boolean value)](#setDoNotSuppressParagraphBorders-boolean-) | 不要抑制框架旁边的段落边框。 |
| [setDoNotUseEastAsianBreakRules(boolean value)](#setDoNotUseEastAsianBreakRules-boolean-) | 使用文档网格时不要压缩可压缩字符。 |
| [setDoNotUseHTMLParagraphAutoSpacing(boolean value)](#setDoNotUseHTMLParagraphAutoSpacing-boolean-) | 为 HTML 自动设置使用固定段落间距。 |
| [setDoNotUseIndentAsNumberingTabStop(boolean value)](#setDoNotUseIndentAsNumberingTabStop-boolean-) | 编号后创建制表位时忽略悬挂缩进。 |
| [setDoNotVertAlignCellWithSp(boolean value)](#setDoNotVertAlignCellWithSp-boolean-) | 不要垂直对齐包含浮动对象的单元格。 |
| [setDoNotVertAlignInTxbx(boolean value)](#setDoNotVertAlignInTxbx-boolean-) | 忽略文本框中的垂直对齐。 |
| [setDoNotWrapTextWithPunct(boolean value)](#setDoNotWrapTextWithPunct-boolean-) | 不允许使用字符网格悬挂标点。 |
| [setFootnoteLayoutLikeWW8(boolean value)](#setFootnoteLayoutLikeWW8-boolean-) | 模拟 Word 6.x/95/97 脚注放置。 |
| [setForgetLastTabAlignment(boolean value)](#setForgetLastTabAlignment-boolean-) | 如果段落未左对齐，则在对齐段落时忽略最后一个制表位的宽度。 |
| [setGrowAutofit(boolean value)](#setGrowAutofit-boolean-) | 允许表格自动适应页边距。 |
| [setLayoutRawTableWidth(boolean value)](#setLayoutRawTableWidth-boolean-) | 在决定表是否应该包裹浮动对象时忽略表前的空格。 |
| [setLayoutTableRowsApart(boolean value)](#setLayoutTableRowsApart-boolean-) | 允许表格行独立包装内联对象。 |
| [setLineWrapLikeWord6(boolean value)](#setLineWrapLikeWord6-boolean-) | 为东亚文本模拟 Word 6.0 换行。 |
| [setMWSmallCaps(boolean value)](#setMWSmallCaps-boolean-) | 模拟 Macintosh Small Caps 格式的 Word 5.x。 |
| [setNoColumnBalance(boolean value)](#setNoColumnBalance-boolean-) | 不要平衡节内的文本列。 |
| [setNoExtraLineSpacing(boolean value)](#setNoExtraLineSpacing-boolean-) | 不要在具有精确行高的行上居中内容。 |
| [setNoLeading(boolean value)](#setNoLeading-boolean-) | 不要在文本行之间添加前导。 |
| [setNoSpaceRaiseLower(boolean value)](#setNoSpaceRaiseLower-boolean-) | 不要增加凸起/降低文本的行高。 |
| [setNoTabHangInd(boolean value)](#setNoTabHangInd-boolean-) | 不要为悬挂缩进创建自定义制表位。 |
| [setOverrideTableStyleFontSizeAndJustification(boolean value)](#setOverrideTableStyleFontSizeAndJustification-boolean-) | 指定如何评估文档的样式层次结构。 |
| [setPrintBodyTextBeforeHeader(boolean value)](#setPrintBodyTextBeforeHeader-boolean-) | 在页眉/页脚内容之前打印正文文本。 |
| [setPrintColBlack(boolean value)](#setPrintColBlack-boolean-) | 将颜色打印为黑色和白色，无需抖动。 |
| [setSelectFldWithFirstOrLastChar(boolean value)](#setSelectFldWithFirstOrLastChar-boolean-) | 选择第一个或最后一个字符时选择字段。 |
| [setShapeLayoutLikeWW8(boolean value)](#setShapeLayoutLikeWW8-boolean-) | 模拟环绕浮动对象的 Word 97 文本。 |
| [setShowBreaksInFrames(boolean value)](#setShowBreaksInFrames-boolean-) | 显示帧中存在的分页符/分栏符。 |
| [setSpaceForUL(boolean value)](#setSpaceForUL-boolean-) | 在基线下方为带下划线的东亚文本添加额外的空间。 |
| [setSpacingInWholePoints(boolean value)](#setSpacingInWholePoints-boolean-) | 仅按整点扩展/压缩文本。 |
| [setSplitPgBreakAndParaMark(boolean value)](#setSplitPgBreakAndParaMark-boolean-) | 总是在分页后将段落标记移动到页面。 |
| [setSubFontBySize(boolean value)](#setSubFontBySize-boolean-) | 在字体替换期间增加字体大小的优先级。 |
| [setSuppressBottomSpacing(boolean value)](#setSuppressBottomSpacing-boolean-) | 忽略页面上最后一行的确切行高。 |
| [setSuppressSpBfAfterPgBrk(boolean value)](#setSuppressSpBfAfterPgBrk-boolean-) | 不要在分页后的第一行之前使用空格。 |
| [setSuppressSpacingAtTopOfPage(boolean value)](#setSuppressSpacingAtTopOfPage-boolean-) | 忽略页面上第一行的最小行高。 |
| [setSuppressTopSpacing(boolean value)](#setSuppressTopSpacing-boolean-) | 忽略页面上第一行的最小和精确行高。 |
| [setSuppressTopSpacingWP(boolean value)](#setSuppressTopSpacingWP-boolean-) | 模拟 WordPerfect 5.x 行间距。 |
| [setSwapBordersFacingPgs(boolean value)](#setSwapBordersFacingPgs-boolean-) | 在奇数页上交换段落边框。 |
| [setSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning(boolean value)](#setSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning-boolean-) |  |
| [setTransparentMetafiles(boolean value)](#setTransparentMetafiles-boolean-) | 指定不空白图元文件图片后面的区域。 |
| [setTruncateFontHeightsLikeWP6(boolean value)](#setTruncateFontHeightsLikeWP6-boolean-) | 模拟 WordPerfect 6.x 字体高度计算。 |
| [setUICompat97To2003(boolean value)](#setUICompat97To2003-boolean-) | **True**禁用与 Word97-2003 不兼容的 UI 功能。 |
| [setUlTrailSpace(boolean value)](#setUlTrailSpace-boolean-) | 在所有尾随空格下划线。 |
| [setUnderlineTabInNumList(boolean value)](#setUnderlineTabInNumList-boolean-) | 在编号后的字符后加下划线。 |
| [setUseAltKinsokuLineBreakRules(boolean value)](#setUseAltKinsokuLineBreakRules-boolean-) | 使用另一种东亚断线规则。 |
| [setUseAnsiKerningPairs(boolean value)](#setUseAnsiKerningPairs-boolean-) | 使用字体中的 ANSI Kerning Pairs。 |
| [setUseFELayout(boolean value)](#setUseFELayout-boolean-) | 不要绕过东亚/复杂脚本布局代码。 |
| [setUseNormalStyleForList(boolean value)](#setUseNormalStyleForList-boolean-) | 不要自动将列表段落样式应用于项目符号/编号文本。 |
| [setUsePrinterMetrics(boolean value)](#setUsePrinterMetrics-boolean-) | 使用打印机度量来显示文档。 |
| [setUseSingleBorderforContiguousCells(boolean value)](#setUseSingleBorderforContiguousCells-boolean-) | 对表格边界冲突使用简化规则。 |
| [setUseWord2002TableStyleRules(boolean value)](#setUseWord2002TableStyleRules-boolean-) | 模拟 Word 2002 表格样式规则。 |
| [setUseWord2010TableStyleRules(boolean value)](#setUseWord2010TableStyleRules-boolean-) |  |
| [setUseWord97LineBreakRules(boolean value)](#setUseWord97LineBreakRules-boolean-) | 模拟 Word 97 东亚换行。 |
| [setWPJustification(boolean value)](#setWPJustification-boolean-) | 模拟 WordPerfect 6.x 段落对齐。 |
| [setWPSpaceWidth(boolean value)](#setWPSpaceWidth-boolean-) | 指定是否像在 WordPerfect 5.x 中那样设置空格的宽度。 |
| [setWrapTrailSpaces(boolean value)](#setWrapTrailSpaces-boolean-) | 换行尾随空格。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### getAdjustLineHeightInTable() {#getAdjustLineHeightInTable--}
```
public boolean getAdjustLineHeightInTable()
```


将文档网格线间距添加到表格单元格中的线。

**退货:**
boolean - 对应的布尔值。
### getAlignTablesRowByRow() {#getAlignTablesRowByRow--}
```
public boolean getAlignTablesRowByRow()
```


独立对齐表格行。

**退货:**
boolean - 对应的布尔值。
### getAllowSpaceOfSameStyleInTable() {#getAllowSpaceOfSameStyleInTable--}
```
public boolean getAllowSpaceOfSameStyleInTable()
```


允许表格中段落的上下文间距。

**退货:**
boolean - 对应的布尔值。
### getApplyBreakingRules() {#getApplyBreakingRules--}
```
public boolean getApplyBreakingRules()
```


使用传统的埃塞俄比亚语和阿姆哈拉语换行规则。

**退货:**
boolean - 对应的布尔值。
### getAutoSpaceLikeWord95() {#getAutoSpaceLikeWord95--}
```
public boolean getAutoSpaceLikeWord95()
```


模拟 Word 95 全角字符间距。

**退货:**
boolean - 对应的布尔值。
### getAutofitToFirstFixedWidthCell() {#getAutofitToFirstFixedWidthCell--}
```
public boolean getAutofitToFirstFixedWidthCell()
```


允许表格列超过组成单元格的首选宽度。该选项在 MS Word 2013 用户界面中称为“使用 Word 2003 表格自动调整规则”。它实际上也会影响固定布局表的网格计算方式（在某些情况下）。

**退货:**
boolean - 对应的布尔值。
### getBalanceSingleByteDoubleByteWidth() {#getBalanceSingleByteDoubleByteWidth--}
```
public boolean getBalanceSingleByteDoubleByteWidth()
```


平衡单字节和双字节字符。

**退货:**
boolean - 对应的布尔值。
### getCachedColBalance() {#getCachedColBalance--}
```
public boolean getCachedColBalance()
```


使用缓存的段落信息进行列平衡。

**退货:**
boolean - 对应的布尔值。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getConvMailMergeEsc() {#getConvMailMergeEsc--}
```
public boolean getConvMailMergeEsc()
```


将反斜杠引号分隔符视为两个引号。

**退货:**
boolean - 对应的布尔值。
### getDisableOpen类型FontFormattingFeatures() {#getDisableOpen类型FontFormattingFeatures--}
```
public boolean getDisableOpen类型FontFormattingFeatures()
```




**退货:**
布尔值
### getDisplayHangulFixedWidth() {#getDisplayHangulFixedWidth--}
```
public boolean getDisplayHangulFixedWidth()
```


始终为韩文字符使用固定宽度。

**退货:**
boolean - 对应的布尔值。
### getDoNotAutofitConstrainedTables() {#getDoNotAutofitConstrainedTables--}
```
public boolean getDoNotAutofitConstrainedTables()
```


不要自动调整表格以适合包裹的对象。

**退货:**
boolean - 对应的布尔值。
### getDoNotBreakConstrainedForcedTable() {#getDoNotBreakConstrainedForcedTable--}
```
public boolean getDoNotBreakConstrainedForcedTable()
```


不要打破浮动表周围的表行。

**退货:**
boolean - 对应的布尔值。
### getDoNotBreakWrappedTables() {#getDoNotBreakWrappedTables--}
```
public boolean getDoNotBreakWrappedTables()
```


不允许浮动表格跨越页面。

**退货:**
boolean - 对应的布尔值。
### getDoNotExpandShiftReturn() {#getDoNotExpandShiftReturn--}
```
public boolean getDoNotExpandShiftReturn()
```


不要证明以软换行符结尾的行。

**退货:**
boolean - 对应的布尔值。
### getDoNotLeaveBackslashAlone() {#getDoNotLeaveBackslashAlone--}
```
public boolean getDoNotLeaveBackslashAlone()
```


输入时将反斜杠转换为日元符号。

**退货:**
boolean - 对应的布尔值。
### getDoNotSnapToGridInCell() {#getDoNotSnapToGridInCell--}
```
public boolean getDoNotSnapToGridInCell()
```


不要在包含对象的表格单元格中对齐文档网格。

**退货:**
boolean - 对应的布尔值。
### getDoNotSuppressIndentation() {#getDoNotSuppressIndentation--}
```
public boolean getDoNotSuppressIndentation()
```


计算段落缩进时不要忽略浮动对象。

**退货:**
boolean - 对应的布尔值。
### getDoNotSuppressParagraphBorders() {#getDoNotSuppressParagraphBorders--}
```
public boolean getDoNotSuppressParagraphBorders()
```


不要抑制框架旁边的段落边框。

**退货:**
boolean - 对应的布尔值。
### getDoNotUseEastAsianBreakRules() {#getDoNotUseEastAsianBreakRules--}
```
public boolean getDoNotUseEastAsianBreakRules()
```


使用文档网格时不要压缩可压缩字符。

**退货:**
boolean - 对应的布尔值。
### getDoNotUseHTMLParagraphAutoSpacing() {#getDoNotUseHTMLParagraphAutoSpacing--}
```
public boolean getDoNotUseHTMLParagraphAutoSpacing()
```


为 HTML 自动设置使用固定段落间距。

**退货:**
boolean - 对应的布尔值。
### getDoNotUseIndentAsNumberingTabStop() {#getDoNotUseIndentAsNumberingTabStop--}
```
public boolean getDoNotUseIndentAsNumberingTabStop()
```


编号后创建制表位时忽略悬挂缩进。

**退货:**
boolean - 对应的布尔值。
### getDoNotVertAlignCellWithSp() {#getDoNotVertAlignCellWithSp--}
```
public boolean getDoNotVertAlignCellWithSp()
```


不要垂直对齐包含浮动对象的单元格。

**退货:**
boolean - 对应的布尔值。
### getDoNotVertAlignInTxbx() {#getDoNotVertAlignInTxbx--}
```
public boolean getDoNotVertAlignInTxbx()
```


忽略文本框中的垂直对齐。

**退货:**
boolean - 对应的布尔值。
### getDoNotWrapTextWithPunct() {#getDoNotWrapTextWithPunct--}
```
public boolean getDoNotWrapTextWithPunct()
```


不允许使用字符网格悬挂标点。

**退货:**
boolean - 对应的布尔值。
### getFootnoteLayoutLikeWW8() {#getFootnoteLayoutLikeWW8--}
```
public boolean getFootnoteLayoutLikeWW8()
```


模拟 Word 6.x/95/97 脚注放置。

**退货:**
boolean - 对应的布尔值。
### getForgetLastTabAlignment() {#getForgetLastTabAlignment--}
```
public boolean getForgetLastTabAlignment()
```


如果段落未左对齐，则在对齐段落时忽略最后一个制表位的宽度。

**退货:**
boolean - 对应的布尔值。
### getGrowAutofit() {#getGrowAutofit--}
```
public boolean getGrowAutofit()
```


允许表格自动适应页边距。

**退货:**
boolean - 对应的布尔值。
### getLayoutRawTableWidth() {#getLayoutRawTableWidth--}
```
public boolean getLayoutRawTableWidth()
```


在决定表是否应该包裹浮动对象时忽略表前的空格。

**退货:**
boolean - 对应的布尔值。
### getLayoutTableRowsApart() {#getLayoutTableRowsApart--}
```
public boolean getLayoutTableRowsApart()
```


允许表格行独立包装内联对象。

**退货:**
boolean - 对应的布尔值。
### getLineWrapLikeWord6() {#getLineWrapLikeWord6--}
```
public boolean getLineWrapLikeWord6()
```


为东亚文本模拟 Word 6.0 换行。

**退货:**
boolean - 对应的布尔值。
### getMWSmallCaps() {#getMWSmallCaps--}
```
public boolean getMWSmallCaps()
```


模拟 Macintosh Small Caps 格式的 Word 5.x。

**退货:**
boolean - 对应的布尔值。
### getNoColumnBalance() {#getNoColumnBalance--}
```
public boolean getNoColumnBalance()
```


不要平衡节内的文本列。

**退货:**
boolean - 对应的布尔值。
### getNoExtraLineSpacing() {#getNoExtraLineSpacing--}
```
public boolean getNoExtraLineSpacing()
```


不要在具有精确行高的行上居中内容。

**退货:**
boolean - 对应的布尔值。
### getNoLeading() {#getNoLeading--}
```
public boolean getNoLeading()
```


不要在文本行之间添加前导。

**退货:**
boolean - 对应的布尔值。
### getNoSpaceRaiseLower() {#getNoSpaceRaiseLower--}
```
public boolean getNoSpaceRaiseLower()
```


不要增加凸起/降低文本的行高。

**退货:**
boolean - 对应的布尔值。
### getNoTabHangInd() {#getNoTabHangInd--}
```
public boolean getNoTabHangInd()
```


不要为悬挂缩进创建自定义制表位。

**退货:**
boolean - 对应的布尔值。
### getOverrideTableStyleFontSizeAndJustification() {#getOverrideTableStyleFontSizeAndJustification--}
```
public boolean getOverrideTableStyleFontSizeAndJustification()
```


指定如何评估文档的样式层次结构。

**退货:**
boolean - 对应的布尔值。
### getPrintBodyTextBeforeHeader() {#getPrintBodyTextBeforeHeader--}
```
public boolean getPrintBodyTextBeforeHeader()
```


在页眉/页脚内容之前打印正文文本。

**退货:**
boolean - 对应的布尔值。
### getPrintColBlack() {#getPrintColBlack--}
```
public boolean getPrintColBlack()
```


将颜色打印为黑色和白色，无需抖动。

**退货:**
boolean - 对应的布尔值。
### getSelectFldWithFirstOrLastChar() {#getSelectFldWithFirstOrLastChar--}
```
public boolean getSelectFldWithFirstOrLastChar()
```


选择第一个或最后一个字符时选择字段。

**退货:**
boolean - 对应的布尔值。
### getShapeLayoutLikeWW8() {#getShapeLayoutLikeWW8--}
```
public boolean getShapeLayoutLikeWW8()
```


模拟环绕浮动对象的 Word 97 文本。

**退货:**
boolean - 对应的布尔值。
### getShowBreaksInFrames() {#getShowBreaksInFrames--}
```
public boolean getShowBreaksInFrames()
```


显示帧中存在的分页符/分栏符。

**退货:**
boolean - 对应的布尔值。
### getSpaceForUL() {#getSpaceForUL--}
```
public boolean getSpaceForUL()
```


在基线下方为带下划线的东亚文本添加额外的空间。

**退货:**
boolean - 对应的布尔值。
### getSpacingInWholePoints() {#getSpacingInWholePoints--}
```
public boolean getSpacingInWholePoints()
```


仅按整点扩展/压缩文本。

**退货:**
boolean - 对应的布尔值。
### getSplitPgBreakAndParaMark() {#getSplitPgBreakAndParaMark--}
```
public boolean getSplitPgBreakAndParaMark()
```


总是在分页后将段落标记移动到页面。

**退货:**
boolean - 对应的布尔值。
### getSubFontBySize() {#getSubFontBySize--}
```
public boolean getSubFontBySize()
```


在字体替换期间增加字体大小的优先级。

**退货:**
boolean - 对应的布尔值。
### getSuppressBottomSpacing() {#getSuppressBottomSpacing--}
```
public boolean getSuppressBottomSpacing()
```


忽略页面上最后一行的确切行高。

**退货:**
boolean - 对应的布尔值。
### getSuppressSpBfAfterPgBrk() {#getSuppressSpBfAfterPgBrk--}
```
public boolean getSuppressSpBfAfterPgBrk()
```


不要在分页后的第一行之前使用空格。

**退货:**
boolean - 对应的布尔值。
### getSuppressSpacingAtTopOfPage() {#getSuppressSpacingAtTopOfPage--}
```
public boolean getSuppressSpacingAtTopOfPage()
```


忽略页面上第一行的最小行高。

**退货:**
boolean - 对应的布尔值。
### getSuppressTopSpacing() {#getSuppressTopSpacing--}
```
public boolean getSuppressTopSpacing()
```


忽略页面上第一行的最小和精确行高。

**退货:**
boolean - 对应的布尔值。
### getSuppressTopSpacingWP() {#getSuppressTopSpacingWP--}
```
public boolean getSuppressTopSpacingWP()
```


模拟 WordPerfect 5.x 行间距。

**退货:**
boolean - 对应的布尔值。
### getSwapBordersFacingPgs() {#getSwapBordersFacingPgs--}
```
public boolean getSwapBordersFacingPgs()
```


在奇数页上交换段落边框。

**退货:**
boolean - 对应的布尔值。
### getSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning() {#getSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning--}
```
public boolean getSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning()
```




**退货:**
布尔值
### getTransparentMetafiles() {#getTransparentMetafiles--}
```
public boolean getTransparentMetafiles()
```


指定不空白图元文件图片后面的区域。

**退货:**
boolean - 对应的布尔值。
### getTruncateFontHeightsLikeWP6() {#getTruncateFontHeightsLikeWP6--}
```
public boolean getTruncateFontHeightsLikeWP6()
```


模拟 WordPerfect 6.x 字体高度计算。

**退货:**
boolean - 对应的布尔值。
### getUICompat97To2003() {#getUICompat97To2003--}
```
public boolean getUICompat97To2003()
```


**True**禁用与 Word97-2003 不兼容的 UI 功能。默认值为**false**.控制禁用与 Word97-2003 不兼容的 UI 功能的 Word97-2003 兼容性设置。什么时候**true**'w:uiCompat97To2003' XML 元素被写入 '\\单词\\settings.xml' 文档包部分。默认值为**false**.当设置为**false**这个元素没有写。从技术上讲，此属性不是兼容性选项的一部分，但我们将其放在这里是为了 API 方便。

**退货:**
boolean - 对应的布尔值。
### getUlTrailSpace() {#getUlTrailSpace--}
```
public boolean getUlTrailSpace()
```


在所有尾随空格下划线。

**退货:**
boolean - 对应的布尔值。
### getUnderlineTabInNumList() {#getUnderlineTabInNumList--}
```
public boolean getUnderlineTabInNumList()
```


在编号后的字符后加下划线。

**退货:**
boolean - 对应的布尔值。
### getUseAltKinsokuLineBreakRules() {#getUseAltKinsokuLineBreakRules--}
```
public boolean getUseAltKinsokuLineBreakRules()
```


使用另一种东亚断线规则。

**退货:**
boolean - 对应的布尔值。
### getUseAnsiKerningPairs() {#getUseAnsiKerningPairs--}
```
public boolean getUseAnsiKerningPairs()
```


使用字体中的 ANSI Kerning Pairs。

**退货:**
boolean - 对应的布尔值。
### getUseFELayout() {#getUseFELayout--}
```
public boolean getUseFELayout()
```


不要绕过东亚/复杂脚本布局代码。

**退货:**
boolean - 对应的布尔值。
### getUseNormalStyleForList() {#getUseNormalStyleForList--}
```
public boolean getUseNormalStyleForList()
```


不要自动将列表段落样式应用于项目符号/编号文本。

**退货:**
boolean - 对应的布尔值。
### getUsePrinterMetrics() {#getUsePrinterMetrics--}
```
public boolean getUsePrinterMetrics()
```


使用打印机度量来显示文档。打印机指标可能因使用的驱动程序而异。例如，Windows“Microsoft OpenXPS 班级 Driver 2”和“Microsoft Print to PDF”提供的指标略有不同。因此，如果启用此选项，最终文档的布局可能会发生变化。

**退货:**
boolean - 对应的布尔值。
### getUseSingleBorderforContiguousCells() {#getUseSingleBorderforContiguousCells--}
```
public boolean getUseSingleBorderforContiguousCells()
```


对表格边界冲突使用简化规则。

**退货:**
boolean - 对应的布尔值。
### getUseWord2002TableStyleRules() {#getUseWord2002TableStyleRules--}
```
public boolean getUseWord2002TableStyleRules()
```


模拟 Word 2002 表格样式规则。

**退货:**
boolean - 对应的布尔值。
### getUseWord2010TableStyleRules() {#getUseWord2010TableStyleRules--}
```
public boolean getUseWord2010TableStyleRules()
```




**退货:**
布尔值
### getUseWord97LineBreakRules() {#getUseWord97LineBreakRules--}
```
public boolean getUseWord97LineBreakRules()
```


模拟 Word 97 东亚换行。

**退货:**
boolean - 对应的布尔值。
### getWPJustification() {#getWPJustification--}
```
public boolean getWPJustification()
```


模拟 WordPerfect 6.x 段落对齐。

**退货:**
boolean - 对应的布尔值。
### getWPSpaceWidth() {#getWPSpaceWidth--}
```
public boolean getWPSpaceWidth()
```


指定是否像在 WordPerfect 5.x 中那样设置空格的宽度。

**退货:**
boolean - 对应的布尔值。
### getWrapTrailSpaces() {#getWrapTrailSpaces--}
```
public boolean getWrapTrailSpaces()
```


换行尾随空格。

**退货:**
boolean - 对应的布尔值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
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




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| version | int |  |

### setAdjustLineHeightInTable(boolean value) {#setAdjustLineHeightInTable-boolean-}
```
public void setAdjustLineHeightInTable(boolean value)
```


将文档网格线间距添加到表格单元格中的线。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setAlignTablesRowByRow(boolean value) {#setAlignTablesRowByRow-boolean-}
```
public void setAlignTablesRowByRow(boolean value)
```


独立对齐表格行。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setAllowSpaceOfSameStyleInTable(boolean value) {#setAllowSpaceOfSameStyleInTable-boolean-}
```
public void setAllowSpaceOfSameStyleInTable(boolean value)
```


允许表格中段落的上下文间距。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setApplyBreakingRules(boolean value) {#setApplyBreakingRules-boolean-}
```
public void setApplyBreakingRules(boolean value)
```


使用传统的埃塞俄比亚语和阿姆哈拉语换行规则。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setAutoSpaceLikeWord95(boolean value) {#setAutoSpaceLikeWord95-boolean-}
```
public void setAutoSpaceLikeWord95(boolean value)
```


模拟 Word 95 全角字符间距。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setAutofitToFirstFixedWidthCell(boolean value) {#setAutofitToFirstFixedWidthCell-boolean-}
```
public void setAutofitToFirstFixedWidthCell(boolean value)
```


允许表格列超过组成单元格的首选宽度。该选项在 MS Word 2013 用户界面中称为“使用 Word 2003 表格自动调整规则”。它实际上也会影响固定布局表的网格计算方式（在某些情况下）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setBalanceSingleByteDoubleByteWidth(boolean value) {#setBalanceSingleByteDoubleByteWidth-boolean-}
```
public void setBalanceSingleByteDoubleByteWidth(boolean value)
```


平衡单字节和双字节字符。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setCachedColBalance(boolean value) {#setCachedColBalance-boolean-}
```
public void setCachedColBalance(boolean value)
```


使用缓存的段落信息进行列平衡。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setConvMailMergeEsc(boolean value) {#setConvMailMergeEsc-boolean-}
```
public void setConvMailMergeEsc(boolean value)
```


将反斜杠引号分隔符视为两个引号。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setDisableOpen类型FontFormattingFeatures(boolean value) {#setDisableOpen类型FontFormattingFeatures-boolean-}
```
public void setDisableOpen类型FontFormattingFeatures(boolean value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean |  |

### setDisplayHangulFixedWidth(boolean value) {#setDisplayHangulFixedWidth-boolean-}
```
public void setDisplayHangulFixedWidth(boolean value)
```


始终为韩文字符使用固定宽度。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setDoNotAutofitConstrainedTables(boolean value) {#setDoNotAutofitConstrainedTables-boolean-}
```
public void setDoNotAutofitConstrainedTables(boolean value)
```


不要自动调整表格以适合包裹的对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setDoNotBreakConstrainedForcedTable(boolean value) {#setDoNotBreakConstrainedForcedTable-boolean-}
```
public void setDoNotBreakConstrainedForcedTable(boolean value)
```


不要打破浮动表周围的表行。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setDoNotBreakWrappedTables(boolean value) {#setDoNotBreakWrappedTables-boolean-}
```
public void setDoNotBreakWrappedTables(boolean value)
```


不允许浮动表格跨越页面。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setDoNotExpandShiftReturn(boolean value) {#setDoNotExpandShiftReturn-boolean-}
```
public void setDoNotExpandShiftReturn(boolean value)
```


不要证明以软换行符结尾的行。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setDoNotLeaveBackslashAlone(boolean value) {#setDoNotLeaveBackslashAlone-boolean-}
```
public void setDoNotLeaveBackslashAlone(boolean value)
```


输入时将反斜杠转换为日元符号。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setDoNotSnapToGridInCell(boolean value) {#setDoNotSnapToGridInCell-boolean-}
```
public void setDoNotSnapToGridInCell(boolean value)
```


不要在包含对象的表格单元格中对齐文档网格。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setDoNotSuppressIndentation(boolean value) {#setDoNotSuppressIndentation-boolean-}
```
public void setDoNotSuppressIndentation(boolean value)
```


计算段落缩进时不要忽略浮动对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setDoNotSuppressParagraphBorders(boolean value) {#setDoNotSuppressParagraphBorders-boolean-}
```
public void setDoNotSuppressParagraphBorders(boolean value)
```


不要抑制框架旁边的段落边框。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setDoNotUseEastAsianBreakRules(boolean value) {#setDoNotUseEastAsianBreakRules-boolean-}
```
public void setDoNotUseEastAsianBreakRules(boolean value)
```


使用文档网格时不要压缩可压缩字符。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setDoNotUseHTMLParagraphAutoSpacing(boolean value) {#setDoNotUseHTMLParagraphAutoSpacing-boolean-}
```
public void setDoNotUseHTMLParagraphAutoSpacing(boolean value)
```


为 HTML 自动设置使用固定段落间距。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setDoNotUseIndentAsNumberingTabStop(boolean value) {#setDoNotUseIndentAsNumberingTabStop-boolean-}
```
public void setDoNotUseIndentAsNumberingTabStop(boolean value)
```


编号后创建制表位时忽略悬挂缩进。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setDoNotVertAlignCellWithSp(boolean value) {#setDoNotVertAlignCellWithSp-boolean-}
```
public void setDoNotVertAlignCellWithSp(boolean value)
```


不要垂直对齐包含浮动对象的单元格。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setDoNotVertAlignInTxbx(boolean value) {#setDoNotVertAlignInTxbx-boolean-}
```
public void setDoNotVertAlignInTxbx(boolean value)
```


忽略文本框中的垂直对齐。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setDoNotWrapTextWithPunct(boolean value) {#setDoNotWrapTextWithPunct-boolean-}
```
public void setDoNotWrapTextWithPunct(boolean value)
```


不允许使用字符网格悬挂标点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setFootnoteLayoutLikeWW8(boolean value) {#setFootnoteLayoutLikeWW8-boolean-}
```
public void setFootnoteLayoutLikeWW8(boolean value)
```


模拟 Word 6.x/95/97 脚注放置。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setForgetLastTabAlignment(boolean value) {#setForgetLastTabAlignment-boolean-}
```
public void setForgetLastTabAlignment(boolean value)
```


如果段落未左对齐，则在对齐段落时忽略最后一个制表位的宽度。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setGrowAutofit(boolean value) {#setGrowAutofit-boolean-}
```
public void setGrowAutofit(boolean value)
```


允许表格自动适应页边距。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setLayoutRawTableWidth(boolean value) {#setLayoutRawTableWidth-boolean-}
```
public void setLayoutRawTableWidth(boolean value)
```


在决定表是否应该包裹浮动对象时忽略表前的空格。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setLayoutTableRowsApart(boolean value) {#setLayoutTableRowsApart-boolean-}
```
public void setLayoutTableRowsApart(boolean value)
```


允许表格行独立包装内联对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setLineWrapLikeWord6(boolean value) {#setLineWrapLikeWord6-boolean-}
```
public void setLineWrapLikeWord6(boolean value)
```


为东亚文本模拟 Word 6.0 换行。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setMWSmallCaps(boolean value) {#setMWSmallCaps-boolean-}
```
public void setMWSmallCaps(boolean value)
```


模拟 Macintosh Small Caps 格式的 Word 5.x。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setNoColumnBalance(boolean value) {#setNoColumnBalance-boolean-}
```
public void setNoColumnBalance(boolean value)
```


不要平衡节内的文本列。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setNoExtraLineSpacing(boolean value) {#setNoExtraLineSpacing-boolean-}
```
public void setNoExtraLineSpacing(boolean value)
```


不要在具有精确行高的行上居中内容。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setNoLeading(boolean value) {#setNoLeading-boolean-}
```
public void setNoLeading(boolean value)
```


不要在文本行之间添加前导。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setNoSpaceRaiseLower(boolean value) {#setNoSpaceRaiseLower-boolean-}
```
public void setNoSpaceRaiseLower(boolean value)
```


不要增加凸起/降低文本的行高。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setNoTabHangInd(boolean value) {#setNoTabHangInd-boolean-}
```
public void setNoTabHangInd(boolean value)
```


不要为悬挂缩进创建自定义制表位。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setOverrideTableStyleFontSizeAndJustification(boolean value) {#setOverrideTableStyleFontSizeAndJustification-boolean-}
```
public void setOverrideTableStyleFontSizeAndJustification(boolean value)
```


指定如何评估文档的样式层次结构。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setPrintBodyTextBeforeHeader(boolean value) {#setPrintBodyTextBeforeHeader-boolean-}
```
public void setPrintBodyTextBeforeHeader(boolean value)
```


在页眉/页脚内容之前打印正文文本。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setPrintColBlack(boolean value) {#setPrintColBlack-boolean-}
```
public void setPrintColBlack(boolean value)
```


将颜色打印为黑色和白色，无需抖动。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSelectFldWithFirstOrLastChar(boolean value) {#setSelectFldWithFirstOrLastChar-boolean-}
```
public void setSelectFldWithFirstOrLastChar(boolean value)
```


选择第一个或最后一个字符时选择字段。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setShapeLayoutLikeWW8(boolean value) {#setShapeLayoutLikeWW8-boolean-}
```
public void setShapeLayoutLikeWW8(boolean value)
```


模拟环绕浮动对象的 Word 97 文本。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setShowBreaksInFrames(boolean value) {#setShowBreaksInFrames-boolean-}
```
public void setShowBreaksInFrames(boolean value)
```


显示帧中存在的分页符/分栏符。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSpaceForUL(boolean value) {#setSpaceForUL-boolean-}
```
public void setSpaceForUL(boolean value)
```


在基线下方为带下划线的东亚文本添加额外的空间。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSpacingInWholePoints(boolean value) {#setSpacingInWholePoints-boolean-}
```
public void setSpacingInWholePoints(boolean value)
```


仅按整点扩展/压缩文本。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSplitPgBreakAndParaMark(boolean value) {#setSplitPgBreakAndParaMark-boolean-}
```
public void setSplitPgBreakAndParaMark(boolean value)
```


总是在分页后将段落标记移动到页面。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSubFontBySize(boolean value) {#setSubFontBySize-boolean-}
```
public void setSubFontBySize(boolean value)
```


在字体替换期间增加字体大小的优先级。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSuppressBottomSpacing(boolean value) {#setSuppressBottomSpacing-boolean-}
```
public void setSuppressBottomSpacing(boolean value)
```


忽略页面上最后一行的确切行高。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSuppressSpBfAfterPgBrk(boolean value) {#setSuppressSpBfAfterPgBrk-boolean-}
```
public void setSuppressSpBfAfterPgBrk(boolean value)
```


不要在分页后的第一行之前使用空格。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSuppressSpacingAtTopOfPage(boolean value) {#setSuppressSpacingAtTopOfPage-boolean-}
```
public void setSuppressSpacingAtTopOfPage(boolean value)
```


忽略页面上第一行的最小行高。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSuppressTopSpacing(boolean value) {#setSuppressTopSpacing-boolean-}
```
public void setSuppressTopSpacing(boolean value)
```


忽略页面上第一行的最小和精确行高。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSuppressTopSpacingWP(boolean value) {#setSuppressTopSpacingWP-boolean-}
```
public void setSuppressTopSpacingWP(boolean value)
```


模拟 WordPerfect 5.x 行间距。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSwapBordersFacingPgs(boolean value) {#setSwapBordersFacingPgs-boolean-}
```
public void setSwapBordersFacingPgs(boolean value)
```


在奇数页上交换段落边框。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning(boolean value) {#setSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning-boolean-}
```
public void setSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning(boolean value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean |  |

### setTransparentMetafiles(boolean value) {#setTransparentMetafiles-boolean-}
```
public void setTransparentMetafiles(boolean value)
```


指定不空白图元文件图片后面的区域。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setTruncateFontHeightsLikeWP6(boolean value) {#setTruncateFontHeightsLikeWP6-boolean-}
```
public void setTruncateFontHeightsLikeWP6(boolean value)
```


模拟 WordPerfect 6.x 字体高度计算。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setUICompat97To2003(boolean value) {#setUICompat97To2003-boolean-}
```
public void setUICompat97To2003(boolean value)
```


**True**禁用与 Word97-2003 不兼容的 UI 功能。默认值为**false**.控制禁用与 Word97-2003 不兼容的 UI 功能的 Word97-2003 兼容性设置。什么时候**true**'w:uiCompat97To2003' XML 元素被写入 '\\单词\\settings.xml' 文档包部分。默认值为**false**.当设置为**false**这个元素没有写。从技术上讲，此属性不是兼容性选项的一部分，但我们将其放在这里是为了 API 方便。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setUlTrailSpace(boolean value) {#setUlTrailSpace-boolean-}
```
public void setUlTrailSpace(boolean value)
```


在所有尾随空格下划线。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setUnderlineTabInNumList(boolean value) {#setUnderlineTabInNumList-boolean-}
```
public void setUnderlineTabInNumList(boolean value)
```


在编号后的字符后加下划线。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setUseAltKinsokuLineBreakRules(boolean value) {#setUseAltKinsokuLineBreakRules-boolean-}
```
public void setUseAltKinsokuLineBreakRules(boolean value)
```


使用另一种东亚断线规则。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setUseAnsiKerningPairs(boolean value) {#setUseAnsiKerningPairs-boolean-}
```
public void setUseAnsiKerningPairs(boolean value)
```


使用字体中的 ANSI Kerning Pairs。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setUseFELayout(boolean value) {#setUseFELayout-boolean-}
```
public void setUseFELayout(boolean value)
```


不要绕过东亚/复杂脚本布局代码。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setUseNormalStyleForList(boolean value) {#setUseNormalStyleForList-boolean-}
```
public void setUseNormalStyleForList(boolean value)
```


不要自动将列表段落样式应用于项目符号/编号文本。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setUsePrinterMetrics(boolean value) {#setUsePrinterMetrics-boolean-}
```
public void setUsePrinterMetrics(boolean value)
```


使用打印机度量来显示文档。打印机指标可能因使用的驱动程序而异。例如，Windows“Microsoft OpenXPS 班级 Driver 2”和“Microsoft Print to PDF”提供的指标略有不同。因此，如果启用此选项，最终文档的布局可能会发生变化。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setUseSingleBorderforContiguousCells(boolean value) {#setUseSingleBorderforContiguousCells-boolean-}
```
public void setUseSingleBorderforContiguousCells(boolean value)
```


对表格边界冲突使用简化规则。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setUseWord2002TableStyleRules(boolean value) {#setUseWord2002TableStyleRules-boolean-}
```
public void setUseWord2002TableStyleRules(boolean value)
```


模拟 Word 2002 表格样式规则。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setUseWord2010TableStyleRules(boolean value) {#setUseWord2010TableStyleRules-boolean-}
```
public void setUseWord2010TableStyleRules(boolean value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean |  |

### setUseWord97LineBreakRules(boolean value) {#setUseWord97LineBreakRules-boolean-}
```
public void setUseWord97LineBreakRules(boolean value)
```


模拟 Word 97 东亚换行。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setWPJustification(boolean value) {#setWPJustification-boolean-}
```
public void setWPJustification(boolean value)
```


模拟 WordPerfect 6.x 段落对齐。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setWPSpaceWidth(boolean value) {#setWPSpaceWidth-boolean-}
```
public void setWPSpaceWidth(boolean value)
```


指定是否像在 WordPerfect 5.x 中那样设置空格的宽度。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setWrapTrailSpaces(boolean value) {#setWrapTrailSpaces-boolean-}
```
public void setWrapTrailSpaces(boolean value)
```


换行尾随空格。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

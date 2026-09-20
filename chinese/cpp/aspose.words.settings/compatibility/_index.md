---
title: "Aspose::Words::Settings::Compatibility enum"
linktitle: "兼容性"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::Compatibility 枚举。指定 C++ 中兼容性选项的名称。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.settings/compatibility/
---
## Compatibility enum


指定兼容性选项的名称。

```cpp
enum class Compatibility
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| NoTabHangInd | 0 | 无 Tab 悬挂缩进。 |
| NoSpaceRaiseLower | 1 | 无空格升降。 |
| SuppressSpBfAfterPgBrk | 2 | 抑制在 [Paragraph](../../aspose.words/paragraph/) 换行前的空格。 |
| WrapTrailSpaces | 3 | 换行尾随空格。 |
| PrintColBlack | 4 | 打印列背景。 |
| NoColumnBalance | 5 | 无列平衡。 |
| ConvMailMergeEsc | 6 | 转换邮件合并转义字符. |
| SuppressTopSpacing | 7 | 抑制顶部间距. |
| UseSingleBorderforContiguousCells | 8 | 对连续单元格使用单一[Border](../../aspose.words/border/). |
| TransparentMetafiles | 9 | 透明元文件. |
| ShowBreaksInFrames | 10 | 在框架中显示换行符. |
| SwapBordersOddFacingPgs | 11 | 在奇数页上交换边框. |
| DoNotLeaveBackslashAlone | 12 | 不要单独留下反斜杠. |
| DoNotExpandOnShiftReturn | 13 | 在 Shift 回车时不要展开. |
| UlTrailSpace | 14 | 为尾随空格添加下划线. |
| BalanceSingleByteDoubleByteWidth | 15 | 平衡单字节和双字节宽度. |
| SuppressTopSpacingAtTopOfPage | 16 | 在 WordPerfect 中抑制顶部行间距. |
| SpacingInWholePoints | 17 | 以整数点为单位的间距. |
| PrintBodyTextBeforeHeader | 18 | 在标题前打印[Body](../../aspose.words/body/)文本. |
| NoLeading | 19 | 无首行缩进。 |
| SpaceForUL | 20 | 下划线的间距。 |
| MWSmallCaps | 21 | MW 小型大写字母。 |
| SuppressTopLineSpacingWP | 22 | 在 WordPerfect 中抑制顶部行间距. |
| TruncateFontHeightLikeWP6 | 23 | 截断 [Font](../../aspose.words/font/) 高度，类似 WordPerfect 6。 |
| SubFontBySize | 24 | 用尺寸替换 [Font](../../aspose.words/font/)。 |
| LineWrapLikeWord6 | 25 | 行换行类似 Word 6。 |
| DoNotSuppressParagraphBorder | 26 | 不要抑制 [Paragraph](../../aspose.words/paragraph/)[Border](../../aspose.words/border/)。 |
| NoExtraLineSpacing | 27 | 无额外行间距。 |
| SuppressBottomSpacing | 28 | 抑制底部间距。 |
| WPSpaceWidth | 29 | WordPerfect 空格宽度。 |
| WPJustification | 30 | WordPerfect 对齐。 |
| UsePrinterMetrics | 31 | 使用打印机度量。 |
| ShapeLayoutLikeWW8 | 32 | 形状 [Layout](../../aspose.words.layout/) 类似 Word 2000。 |
| FootnoteLayoutLikeWW8 | 33 | 脚注 [Layout](../../aspose.words.layout/) 类似 Word 2000。 |
| DoNotUseHtmlParagraphAutoSpacing | 34 | 不要使用 HTML [Paragraph](../../aspose.words/paragraph/) 自动间距。 |
| AdjustLineHeightInTable | 35 | 调整表格中的行高。 |
| ForgetLastTabAlignment | 36 | 忘记上一次制表符对齐。 |
| AutoSpaceLikeWord95 | 37 | 自动空格类似 Word 95。 |
| AlignTableRowByRow | 38 | 按规则对齐表格行。 |
| LayoutRawTableWidth | 39 | [Layout](../../aspose.words.layout/) 原始表格宽度。 |
| LayoutTableRowsApart | 40 | [Layout](../../aspose.words.layout/) 表格行间距。 |
| UseWord97LineBreakRules | 41 | 使用 Word 97 换行规则。 |
| DoNotBreakWrappedTables | 42 | 不要拆分换行的[Tables](../../aspose.words.tables/)。 |
| doNotSnapToGridInCell | 43 | 不要在单元格中对齐到网格。 |
| SelectFldWithFirstOrLastChar | 44 | 选择首字符或尾字符的字段。 |
| ApplyBreakingRules | 45 | 应用断行规则。 |
| DoNotWrapTextWithPunct | 46 | 不要在标点符号处换行文本。 |
| DoNotUseEastAsianBreakRules | 47 | 不要使用东亚断行规则。 |
| UseWord2002TableStyleRules | 48 | 使用 Word 2002 表格[Style](../../aspose.words/style/)规则。 |
| GrowAutofit | 49 | 增长自动适应。 |
| UseNormalStyleForList | 50 | 在列表中使用普通 [Style](../../aspose.words/style/)。 |
| DoNotUseIndentAsNumberingTabStop | 51 | 不要使用缩进作为编号制表位。 |
| UseAltKinsokuLineBreakRules | 52 | 使用 Alt Kinsoku 换行规则。 |
| AllowSpaceOfSameStyleInTable | 53 | 在表格中允许相同 [Style](../../aspose.words/style/) 的空格。 |
| DoNotSuppressIndentation | 54 | 不要抑制缩进。 |
| DoNotAutofitConstrainedTables | 55 | 不要自动适应受约束的 [Tables](../../aspose.words.tables/)。 |
| AutofitToFirstFixedWidthCell | 56 | 自动适应第一个固定宽度单元格。 |
| UnderlineTabInNumList | 57 | 在编号列表中为制表符加下划线。 |
| DisplayHangulFixedWidth | 58 | 显示韩文固定宽度。 |
| SplitPgBreakAndParaMark | 59 | 拆分分页符和 [Paragraph](../../aspose.words/paragraph/) 标记。 |
| DoNotVertAlignCellWithSp | 60 | 不要使用间距垂直对齐单元格。 |
| DoNotBreakConstrainedForcedTable | 61 | 不要拆分受约束的强制 [Tables](../../aspose.words.tables/)。 |
| DoNotVertAlignInTxbx | 62 | 不要在文本框中垂直对齐。 |
| UseAnsiKerningPairs | 63 | 使用 ANSI 字距对。 |
| CachedColBalance | 64 | 已缓存列平衡。 |
| UseFELayout | 65 | 使用 Far East [Layout](../../aspose.words.layout/)。 |
| UICompat97To2003 | 66 | 从 Word 97 到 Word 2003 的用户界面兼容模式。 |
| OverrideTableStyleFontSizeAndJustification | 67 | 覆盖表格 [Style](../../aspose.words/style/)[Font](../../aspose.words/font/) 大小和对齐方式。 |
| DisableOpenTypeFontFormattingFeatures | 68 | 禁用 OpenType [Font](../../aspose.words/font/) 格式化功能。 |
| SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning | 69 | 交换内部和外部以实现镜像缩进和相对定位。 |
| UseWord2010TableStyleRules | 70 | 使用 Word 2010 表格 [Style](../../aspose.words/style/) 规则。 |

## 另见

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)

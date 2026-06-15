---
title: Compatibility enumeration
linktitle: Compatibility enumeration
articleTitle: Compatibility enumeration
second_title: Aspose.Words for Python
description: "aspose.words.settings.Compatibility enumeration. Specifies names of compatibility options."
type: docs
weight: 10
url: /python-net/aspose.words.settings/compatibility/
---

## Compatibility enumeration

Specifies names of compatibility options.


### Members

| Name | Description |
| --- | --- |
| NO_TAB_HANG_IND | No Tab Hang Indent |
| NO_SPACE_RAISE_LOWER | No Space Raise Lower |
| SUPPRESS_SP_BF_AFTER_PG_BRK | Suppress Space Before Paragraph Break |
| WRAP_TRAIL_SPACES | Wrap Trailing Spaces |
| PRINT_COL_BLACK | Print Column Background |
| NO_COLUMN_BALANCE | No Column Balancing |
| CONV_MAIL_MERGE_ESC | Convert Mail Merge Escapes |
| SUPPRESS_TOP_SPACING | Suppress Top Spacing |
| USE_SINGLE_BORDERFOR_CONTIGUOUS_CELLS | Use Single Border for Contiguous Cells |
| TRANSPARENT_METAFILES | Transparent Metafiles |
| SHOW_BREAKS_IN_FRAMES | Show Breaks in Frames |
| SWAP_BORDERS_ODD_FACING_PGS | Swap Borders on Odd-Facing Pages |
| DO_NOT_LEAVE_BACKSLASH_ALONE | Do Not Leave Backslash Alone |
| DO_NOT_EXPAND_ON_SHIFT_RETURN | Do Not Expand on Shift Return |
| UL_TRAIL_SPACE | Underline Trailing Space |
| BALANCE_SINGLE_BYTE_DOUBLE_BYTE_WIDTH | Balance Single-Byte and Double-Byte Widths |
| SUPPRESS_TOP_SPACING_AT_TOP_OF_PAGE | Suppress Top Line Spacing in WordPerfect |
| SPACING_IN_WHOLE_POINTS | Spacing in Whole Points |
| PRINT_BODY_TEXT_BEFORE_HEADER | Print Body Text Before Header |
| NO_LEADING | No Leading |
| SPACE_FOR_UL | Space for Underline |
| MW_SMALL_CAPS | MW Small Caps |
| SUPPRESS_TOP_LINE_SPACING_WP | Suppress Top Line Spacing in WordPerfect |
| TRUNCATE_FONT_HEIGHT_LIKE_WP6 | Truncate Font Height Like WordPerfect 6 |
| SUB_FONT_BY_SIZE | Substitute Font by Size |
| LINE_WRAP_LIKE_WORD6 | Line Wrap Like Word 6 |
| DO_NOT_SUPPRESS_PARAGRAPH_BORDER | Do Not Suppress Paragraph Border |
| NO_EXTRA_LINE_SPACING | No Extra Line Spacing |
| SUPPRESS_BOTTOM_SPACING | Suppress Bottom Spacing |
| WP_SPACE_WIDTH | WordPerfect Space Width |
| WP_JUSTIFICATION | WordPerfect Justification |
| USE_PRINTER_METRICS | Use Printer Metrics |
| SHAPE_LAYOUT_LIKE_WW8 | Shape Layout Like Word 2000 |
| FOOTNOTE_LAYOUT_LIKE_WW8 | Footnote Layout Like Word 2000 |
| DO_NOT_USE_HTML_PARAGRAPH_AUTO_SPACING | Do Not Use HTML Paragraph Auto Spacing |
| ADJUST_LINE_HEIGHT_IN_TABLE | Adjust Line Height in Table |
| FORGET_LAST_TAB_ALIGNMENT | Forget Last Tab Alignment |
| AUTO_SPACE_LIKE_WORD95 | Auto Space Like Word 95 |
| ALIGN_TABLE_ROW_BY_ROW | Align Table Rows by Rule |
| LAYOUT_RAW_TABLE_WIDTH | Layout Raw Table Width |
| LAYOUT_TABLE_ROWS_APART | Layout Table Rows Apart |
| USE_WORD97_LINE_BREAK_RULES | Use Word 97 Line Break Rules |
| DO_NOT_BREAK_WRAPPED_TABLES | Do Not Break Wrapped Tables |
| DO_NOT_SNAP_TO_GRID_IN_CELL | Do Not Snap to Grid in Cells |
| SELECT_FLD_WITH_FIRST_OR_LAST_CHAR | Select Field with First or Last Character |
| APPLY_BREAKING_RULES | Apply Breaking Rules |
| DO_NOT_WRAP_TEXT_WITH_PUNCT | Do Not Wrap Text with Punctuation |
| DO_NOT_USE_EAST_ASIAN_BREAK_RULES | Do Not Use East Asian Break Rules |
| USE_WORD2002_TABLE_STYLE_RULES | Use Word 2002 Table Style Rules |
| GROW_AUTOFIT | Grow AutoFit |
| USE_NORMAL_STYLE_FOR_LIST | Use Normal Style for List |
| DO_NOT_USE_INDENT_AS_NUMBERING_TAB_STOP | Do Not Use Indent as Numbering Tab Stop |
| USE_ALT_KINSOKU_LINE_BREAK_RULES | Use Alt Kinsoku Line Break Rules |
| ALLOW_SPACE_OF_SAME_STYLE_IN_TABLE | Allow Space of Same Style in Table |
| DO_NOT_SUPPRESS_INDENTATION | Do Not Suppress Indentation |
| DO_NOT_AUTOFIT_CONSTRAINED_TABLES | Do Not AutoFit Constrained Tables |
| AUTOFIT_TO_FIRST_FIXED_WIDTH_CELL | AutoFit to First Fixed-Width Cell |
| UNDERLINE_TAB_IN_NUM_LIST | Underline Tab in Numbered List |
| DISPLAY_HANGUL_FIXED_WIDTH | Display Hangul Fixed Width |
| SPLIT_PG_BREAK_AND_PARA_MARK | Split Page Break and Paragraph Mark |
| DO_NOT_VERT_ALIGN_CELL_WITH_SP | Do Not Vertically Align Cell with Spacing |
| DO_NOT_BREAK_CONSTRAINED_FORCED_TABLE | Do Not Break Constrained Forced Tables |
| DO_NOT_VERT_ALIGN_IN_TXBX | Do Not Vertically Align in Textboxes |
| USE_ANSI_KERNING_PAIRS | Use ANSI Kerning Pairs |
| CACHED_COL_BALANCE | Cached Column Balancing |
| USE_FE_LAYOUT | Use Far East Layout |
| UI_COMPAT_97_TO_2003 | User Interface Compatibility Mode from Word 97 to Word 2003 |
| OVERRIDE_TABLE_STYLE_FONT_SIZE_AND_JUSTIFICATION | Override Table Style Font Size and Justification |
| DISABLE_OPEN_TYPE_FONT_FORMATTING_FEATURES | Disable OpenType Font Formatting Features |
| SWAP_INSIDE_AND_OUTSIDE_FOR_MIRROR_INDENTS_AND_RELATIVE_POSITIONING | Swap Inside and Outside for Mirror Indents and Relative Positioning |
| USE_WORD2010_TABLE_STYLE_RULES | Use Word 2010 Table Style Rules |

### Examples

Shows how to optimize the document for different versions of Microsoft Word.

```python
def test_optimize_for(self):
    doc = aw.Document()
    # This object contains an extensive list of flags unique to each document
    # that allow us to facilitate backward compatibility with older versions of Microsoft Word.
    options = doc.compatibility_options
    # Print the default settings for a blank document.
    print('\nDefault optimization settings:')
    ExCompatibilityOptions._print_compatibility_options(options)
    # We can access these settings in Microsoft Word via "File" -> "Options" -> "Advanced" -> "Compatibility options for...".
    doc.save(file_name=ARTIFACTS_DIR + 'CompatibilityOptions.OptimizeFor.DefaultSettings.docx')
    # We can use the OptimizeFor method to ensure optimal compatibility with a specific Microsoft Word version.
    doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2010)
    print('\nOptimized for Word 2010:')
    ExCompatibilityOptions._print_compatibility_options(options)
    doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2000)
    print('\nOptimized for Word 2000:')
    ExCompatibilityOptions._print_compatibility_options(options)

@staticmethod
def _print_compatibility_options(options):
    enabled_options = []
    disabled_options = []
    ExCompatibilityOptions._add_option_name(options.adjust_line_height_in_table, 'AdjustLineHeightInTable', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.align_tables_row_by_row, 'AlignTablesRowByRow', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.allow_space_of_same_style_in_table, 'AllowSpaceOfSameStyleInTable', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.apply_breaking_rules, 'ApplyBreakingRules', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.auto_space_like_word95, 'AutoSpaceLikeWord95', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.autofit_to_first_fixed_width_cell, 'AutofitToFirstFixedWidthCell', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.balance_single_byte_double_byte_width, 'BalanceSingleByteDoubleByteWidth', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.cached_col_balance, 'CachedColBalance', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.conv_mail_merge_esc, 'ConvMailMergeEsc', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.disable_open_type_font_formatting_features, 'DisableOpenTypeFontFormattingFeatures', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.display_hangul_fixed_width, 'DisplayHangulFixedWidth', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.do_not_autofit_constrained_tables, 'DoNotAutofitConstrainedTables', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.do_not_break_constrained_forced_table, 'DoNotBreakConstrainedForcedTable', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.do_not_break_wrapped_tables, 'DoNotBreakWrappedTables', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.do_not_expand_shift_return, 'DoNotExpandShiftReturn', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.do_not_leave_backslash_alone, 'DoNotLeaveBackslashAlone', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.do_not_snap_to_grid_in_cell, 'DoNotSnapToGridInCell', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.do_not_suppress_indentation, 'DoNotSnapToGridInCell', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.do_not_suppress_paragraph_borders, 'DoNotSuppressParagraphBorders', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.do_not_use_east_asian_break_rules, 'DoNotUseEastAsianBreakRules', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.do_not_use_html_paragraph_auto_spacing, 'DoNotUseHTMLParagraphAutoSpacing', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.do_not_use_indent_as_numbering_tab_stop, 'DoNotUseIndentAsNumberingTabStop', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.do_not_vert_align_cell_with_sp, 'DoNotVertAlignCellWithSp', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.do_not_vert_align_in_txbx, 'DoNotVertAlignInTxbx', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.do_not_wrap_text_with_punct, 'DoNotWrapTextWithPunct', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.footnote_layout_like_ww8, 'FootnoteLayoutLikeWW8', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.forget_last_tab_alignment, 'ForgetLastTabAlignment', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.grow_autofit, 'GrowAutofit', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.layout_raw_table_width, 'LayoutRawTableWidth', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.layout_table_rows_apart, 'LayoutTableRowsApart', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.line_wrap_like_word6, 'LineWrapLikeWord6', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.mw_small_caps, 'MWSmallCaps', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.no_column_balance, 'NoColumnBalance', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.no_extra_line_spacing, 'NoExtraLineSpacing', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.no_leading, 'NoLeading', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.no_space_raise_lower, 'NoSpaceRaiseLower', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.no_tab_hang_ind, 'NoTabHangInd', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.override_table_style_font_size_and_justification, 'OverrideTableStyleFontSizeAndJustification', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.print_body_text_before_header, 'PrintBodyTextBeforeHeader', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.print_col_black, 'PrintColBlack', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.select_fld_with_first_or_last_char, 'SelectFldWithFirstOrLastChar', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.shape_layout_like_ww8, 'ShapeLayoutLikeWW8', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.show_breaks_in_frames, 'ShowBreaksInFrames', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.space_for_ul, 'SpaceForUL', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.spacing_in_whole_points, 'SpacingInWholePoints', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.split_pg_break_and_para_mark, 'SplitPgBreakAndParaMark', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.sub_font_by_size, 'SubFontBySize', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.suppress_bottom_spacing, 'SuppressBottomSpacing', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.suppress_sp_bf_after_pg_brk, 'SuppressSpBfAfterPgBrk', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.suppress_spacing_at_top_of_page, 'SuppressSpacingAtTopOfPage', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.suppress_top_spacing, 'SuppressTopSpacing', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.suppress_top_spacing_wp, 'SuppressTopSpacingWP', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.swap_borders_facing_pgs, 'SwapBordersFacingPgs', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.swap_inside_and_outside_for_mirror_indents_and_relative_positioning, 'SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.transparent_metafiles, 'TransparentMetafiles', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.truncate_font_heights_like_wp6, 'TruncateFontHeightsLikeWP6', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.ui_compat_97_to_2003, 'UICompat97To2003', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.ul_trail_space, 'UlTrailSpace', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.underline_tab_in_num_list, 'UnderlineTabInNumList', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.use_alt_kinsoku_line_break_rules, 'UseAltKinsokuLineBreakRules', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.use_ansi_kerning_pairs, 'UseAnsiKerningPairs', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.use_fe_layout, 'UseFELayout', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.use_normal_style_for_list, 'UseNormalStyleForList', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.use_printer_metrics, 'UsePrinterMetrics', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.use_single_borderfor_contiguous_cells, 'UseSingleBorderforContiguousCells', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.use_word2002_table_style_rules, 'UseWord2002TableStyleRules', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.use_word2010_table_style_rules, 'UseWord2010TableStyleRules', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.use_word97_line_break_rules, 'UseWord97LineBreakRules', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.wp_justification, 'WPJustification', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.wp_space_width, 'WPSpaceWidth', enabled_options, disabled_options)
    ExCompatibilityOptions._add_option_name(options.wrap_trail_spaces, 'WrapTrailSpaces', enabled_options, disabled_options)
    print('\tEnabled options:')
    for option_name in enabled_options:
        print(f'\t\t{option_name}')
    print('\tDisabled options:')
    for option_name in disabled_options:
        print(f'\t\t{option_name}')

@staticmethod
def _add_option_name(option, option_name, enabled_options, disabled_options):
    if option:
        enabled_options.append(option_name)
    else:
        disabled_options.append(option_name)
```

### See Also

* module [aspose.words.settings](../)


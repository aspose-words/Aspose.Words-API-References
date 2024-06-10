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
def optimize_for():
    doc = aw.Document()
    # This object contains an extensive list of flags unique to each document
    # that allow us to facilitate backward compatibility with older versions of Microsoft Word.
    options = doc.compatibility_options
    # Print the default settings for a blank document.
    print('\nDefault optimization settings:')
    print_compatibility_options(options)
    # We can access these settings in Microsoft Word via "File" -> "Options" -> "Advanced" -> "Compatibility options for...".
    doc.save(ARTIFACTS_DIR + 'CompatibilityOptions.optimize_for.default_settings.docx')
    # We can use the OptimizeFor method to ensure optimal compatibility with a specific Microsoft Word version.
    doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2010)
    print('\nOptimized for Word 2010:')
    print_compatibility_options(options)
    doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2000)
    print('\nOptimized for Word 2000:')
    print_compatibility_options(options)

def print_compatibility_options(options: aw.settings.CompatibilityOptions):
    """Groups all flags in a document's compatibility options object by state, then prints each group."""
    for enabled in (True, False):
        print('\tEnabled options:' if enabled else '\tDisabled options:')
        for opt in dir(options):
            if not opt.startswith('__') and (not callable(getattr(options, opt))) and (getattr(options, opt) == enabled):
                print(f'\t\t{opt}')
```

### See Also

* module [aspose.words.settings](../)


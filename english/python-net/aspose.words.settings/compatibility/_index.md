---
title: Compatibility enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies names of compatibility options."
type: docs
weight: 10
url: /python-net/aspose.words.settings/compatibility/
---

## Compatibility enumeration

Specifies names of compatibility options.


### Members

| Name | Description |
| --- | --- |
| NO_TAB_HANG_IND |  |
| NO_SPACE_RAISE_LOWER |  |
| SUPPRESS_SP_BF_AFTER_PG_BRK |  |
| WRAP_TRAIL_SPACES |  |
| PRINT_COL_BLACK |  |
| NO_COLUMN_BALANCE |  |
| CONV_MAIL_MERGE_ESC |  |
| SUPPRESS_TOP_SPACING |  |
| USE_SINGLE_BORDERFOR_CONTIGUOUS_CELLS |  |
| TRANSPARENT_METAFILES |  |
| SHOW_BREAKS_IN_FRAMES |  |
| SWAP_BORDERS_ODD_FACING_PGS |  |
| DO_NOT_LEAVE_BACKSLASH_ALONE |  |
| DO_NOT_EXPAND_ON_SHIFT_RETURN |  |
| UL_TRAIL_SPACE |  |
| BALANCE_SINGLE_BYTE_DOUBLE_BYTE_WIDTH |  |
| SUPPRESS_TOP_SPACING_AT_TOP_OF_PAGE |  |
| SPACING_IN_WHOLE_POINTS |  |
| PRINT_BODY_TEXT_BEFORE_HEADER |  |
| NO_LEADING |  |
| SPACE_FOR_UL |  |
| MW_SMALL_CAPS |  |
| SUPPRESS_TOP_LINE_SPACING_WP |  |
| TRUNCATE_FONT_HEIGHT_LIKE_WP6 |  |
| SUB_FONT_BY_SIZE |  |
| LINE_WRAP_LIKE_WORD6 |  |
| DO_NOT_SUPPRESS_PARAGRAPH_BORDER |  |
| NO_EXTRA_LINE_SPACING |  |
| SUPPRESS_BOTTOM_SPACING |  |
| WP_SPACE_WIDTH |  |
| WP_JUSTIFICATION |  |
| USE_PRINTER_METRICS |  |
| SHAPE_LAYOUT_LIKE_WW8 |  |
| FOOTNOTE_LAYOUT_LIKE_WW8 |  |
| DO_NOT_USE_HTML_PARAGRAPH_AUTO_SPACING |  |
| ADJUST_LINE_HEIGHT_IN_TABLE |  |
| FORGET_LAST_TAB_ALIGNMENT |  |
| AUTO_SPACE_LIKE_WORD95 |  |
| ALIGN_TABLE_ROW_BY_ROW |  |
| LAYOUT_RAW_TABLE_WIDTH |  |
| LAYOUT_TABLE_ROWS_APART |  |
| USE_WORD97_LINE_BREAK_RULES |  |
| DO_NOT_BREAK_WRAPPED_TABLES |  |
| DO_NOT_SNAP_TO_GRID_IN_CELL |  |
| SELECT_FLD_WITH_FIRST_OR_LAST_CHAR |  |
| APPLY_BREAKING_RULES |  |
| DO_NOT_WRAP_TEXT_WITH_PUNCT |  |
| DO_NOT_USE_EAST_ASIAN_BREAK_RULES |  |
| USE_WORD2002_TABLE_STYLE_RULES |  |
| GROW_AUTOFIT |  |
| USE_NORMAL_STYLE_FOR_LIST |  |
| DO_NOT_USE_INDENT_AS_NUMBERING_TAB_STOP |  |
| USE_ALT_KINSOKU_LINE_BREAK_RULES |  |
| ALLOW_SPACE_OF_SAME_STYLE_IN_TABLE |  |
| DO_NOT_SUPPRESS_INDENTATION |  |
| DO_NOT_AUTOFIT_CONSTRAINED_TABLES |  |
| AUTOFIT_TO_FIRST_FIXED_WIDTH_CELL |  |
| UNDERLINE_TAB_IN_NUM_LIST |  |
| DISPLAY_HANGUL_FIXED_WIDTH |  |
| SPLIT_PG_BREAK_AND_PARA_MARK |  |
| DO_NOT_VERT_ALIGN_CELL_WITH_SP |  |
| DO_NOT_BREAK_CONSTRAINED_FORCED_TABLE |  |
| DO_NOT_VERT_ALIGN_IN_TXBX |  |
| USE_ANSI_KERNING_PAIRS |  |
| CACHED_COL_BALANCE |  |
| USE_FE_LAYOUT |  |
| UI_COMPAT_97_TO_2003 |  |
| OVERRIDE_TABLE_STYLE_FONT_SIZE_AND_JUSTIFICATION |  |
| DISABLE_OPEN_TYPE_FONT_FORMATTING_FEATURES |  |
| SWAP_INSIDE_AND_OUTSIDE_FOR_MIRROR_INDENTS_AND_RELATIVE_POSITIONING |  |
| USE_WORD2010_TABLE_STYLE_RULES |  |

### Examples

Shows how to optimize the document for different versions of Microsoft Word.

```python
def test_optimize_for(self):

    doc = aw.Document()

    # This object contains an extensive list of flags unique to each document
    # that allow us to facilitate backward compatibility with older versions of Microsoft Word.
    options = doc.compatibility_options

    # Print the default settings for a blank document.
    print("\nDefault optimization settings:")
    ExCompatibilityOptions.print_compatibility_options(options)

    # We can access these settings in Microsoft Word via "File" -> "Options" -> "Advanced" -> "Compatibility options for...".
    doc.save(ARTIFACTS_DIR + "CompatibilityOptions.optimize_for.default_settings.docx")

    # We can use the OptimizeFor method to ensure optimal compatibility with a specific Microsoft Word version.
    doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2010)
    print("\nOptimized for Word 2010:")
    ExCompatibilityOptions.print_compatibility_options(options)

    doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2000)
    print("\nOptimized for Word 2000:")
    ExCompatibilityOptions.print_compatibility_options(options)

@staticmethod
def print_compatibility_options(options: aw.settings.CompatibilityOptions):
    """Groups all flags in a document's compatibility options object by state, then prints each group."""

    for enabled in (True, False):
        print("\tEnabled options:" if enabled else "\tDisabled options:")
        for opt in dir(options):
            if not opt.startswith('__') and not callable(getattr(options, opt)) and getattr(options, opt) == enabled:
                print(f"\t\t{opt}")
```

### See Also

* module [aspose.words.settings](../)


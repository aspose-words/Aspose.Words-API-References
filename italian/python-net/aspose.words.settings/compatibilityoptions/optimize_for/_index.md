---
title: CompatibilityOptions.optimize_for method
linktitle: optimize_for method
articleTitle: optimize_for method
second_title: Aspose.Words for Python
description: "CompatibilityOptions.optimize_for method. Allows to optimize the document contents as well as default Aspose.Words behavior to a particular versions of MS Word."
type: docs
weight: 720
url: /it/python-net/aspose.words.settings/compatibilityoptions/optimize_for/
---

## optimize_for(version) {#mswordversion}

Allows to optimize the document contents as well as default Aspose.Words behavior to a particular versions of MS Word.

Use this method to prevent MS Word from displaying "Compatibility mode" ribbon upon document loading.
(Note that you may also need to set the [OoxmlSaveOptions.compliance](../../../aspose.words.saving/ooxmlsaveoptions/compliance/) property to
[OoxmlCompliance.ISO29500_2008_TRANSITIONAL](../../../aspose.words.saving/ooxmlcompliance/#ISO29500_2008_TRANSITIONAL) or higher.)





```python
def optimize_for(self, version: aspose.words.settings.MsWordVersion):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| version | [MsWordVersion](../../mswordversion/) |  |

### Examples

Shows how to optimize the document for different versions of Microsoft Word.

```python
def test_optimize_for(self):
    doc = aw.Document()
    # Questo oggetto contiene un elenco esteso di flag unici per ogni documento
    # che ci consentono di facilitare la retrocompatibilità con versioni precedenti di Microsoft Word.
    options = doc.compatibility_options
    # Stampa le impostazioni predefinite per un documento vuoto.
    print('\nDefault optimization settings:')
    ExCompatibilityOptions._print_compatibility_options(options)
    # Possiamo accedere a queste impostazioni in Microsoft Word tramite "File" -> "Opzioni" -> "Avanzate" -> "Opzioni di compatibilità per...".
    doc.save(file_name=ARTIFACTS_DIR + 'CompatibilityOptions.OptimizeFor.DefaultSettings.docx')
    # Possiamo utilizzare il metodo OptimizeFor per garantire la compatibilità ottimale con una specifica versione di Microsoft Word.
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

Shows how to set an OOXML compliance specification for a saved document to adhere to.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Se configuriamo le opzioni di compatibilità per conformarci a Microsoft Word 2003,
# l'inserimento di un'immagine definirà la sua forma usando VML.
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2003)
builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
self.assertEqual(aw.drawing.ShapeMarkupLanguage.VML, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().markup_language)
# Lo standard OOXML "ISO/IEC 29500:2008" non supporta le forme VML.
# Se impostiamo la proprietà "Compliance" dell'oggetto SaveOptions su "OoxmlCompliance.Iso29500_2008_Strict",
# qualsiasi documento che salviamo passando questo oggetto dovrà rispettare quello standard.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
save_options.save_format = aw.SaveFormat.DOCX
doc.save(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.Iso29500Strict.docx', save_options=save_options)
# Il nostro documento salvato definisce la forma usando DML per aderire allo standard OOXML "ISO/IEC 29500:2008".
doc = aw.Document(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.Iso29500Strict.docx')
self.assertEqual(aw.drawing.ShapeMarkupLanguage.DML, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().markup_language)
```

Shows how to vertically align the text contents of a text box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=200, height=200)
# Imposta la proprietà "VerticalAnchor" su "TextBoxAnchor.Top" per
# allineare il testo in questa casella di testo con il lato superiore della forma.
# Imposta la proprietà "VerticalAnchor" su "TextBoxAnchor.Middle" per
# allineare il testo in questa casella di testo al centro della forma.
# Imposta la proprietà "VerticalAnchor" a "TextBoxAnchor.Bottom" per
# allineare il testo in questa casella di testo al fondo della forma.
shape.text_box.vertical_anchor = vertical_anchor
builder.move_to(shape.first_paragraph)
builder.write('Hello world!')
# L'allineamento verticale del testo all'interno delle caselle di testo è disponibile da Microsoft Word 2007 in poi.
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2007)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.VerticalAnchor.docx')
```

### See Also

* module [aspose.words.settings](../../)
* class [CompatibilityOptions](../)


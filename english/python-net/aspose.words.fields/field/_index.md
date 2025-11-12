---
title: Field class
linktitle: Field class
articleTitle: Field class
second_title: Aspose.Words for Python
description: "aspose.words.fields.Field class. Represents a Microsoft Word document field"
type: docs
weight: 50
url: /python-net/aspose.words.fields/field/
---

## Field class

Represents a Microsoft Word document field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

A field in a Word document is a complex structure consisting of multiple nodes that include field start,
field code, field separator, field result and field end. Fields can be nested, contain rich content and span
multiple paragraphs or sections in a document. The [Field](./) class is a "facade" object that provides
properties and methods that allow to work with a field as a single object. 

The [Field.start](./start/), [Field.separator](./separator/) and [Field.end](./end/) properties point to the
field start, separator and end nodes of the field respectively.

The content between the field start and separator is the field code. The content between the
field separator and field end is the field result. The field code typically consists of one or more
[Run](../../aspose.words/run/) objects that specify instructions. The processing application is expected to execute
the field code to calculate the field result.

The process of calculating field results is called the field update. Aspose.Words can update field
results of most of the field types in exactly the same way as Microsoft Word does it. Most notably,
Aspose.Words can calculate results of even the most complex formula fields. To calculate the field
result of a single field use the [Field.update()](./update/#default) method. To update fields in the whole document
use [Document.update_fields()](../../aspose.words/document/update_fields/#default).

You can get the plain text version of the field code using the [Field.get_field_code()](./get_field_code/#bool) method.
You can get and set the plain text version of the field result using the [Field.result](./result/) property.
Both the field code and field result can contain complex content, such as nested fields, paragraphs, shapes,
tables and in this case you might want to work with the field nodes directly if you need more control.

You do not create instances of the [Field](./) class directly.
To create a new field use the [DocumentBuilder.insert_field()](../../aspose.words/documentbuilder/insert_field/#str) method.




### Properties

| Name | Description |
| --- | --- |
| [display_result](./display_result/) | Gets the text that represents the displayed field result. |
| [end](./end/) | Gets the node that represents the field end. |
| [format](./format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [is_dirty](./is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [is_locked](./is_locked/) | Gets or sets whether the field is locked (should not recalculate its result). |
| [locale_id](./locale_id/) | Gets or sets the LCID of the field. |
| [result](./result/) | Gets or sets text that is between the field separator and field end. |
| [separator](./separator/) | Gets the node that represents the field separator. Can be ``None``. |
| [start](./start/) | Gets the node that represents the start of the field. |
| [type](./type/) | Gets the Microsoft Word field type. |

### Methods

| Name | Description |
| --- | --- |
|[ as_field()](./as_field/#default) | Cast Field to [Field](./). |
|[ as_field_add_in()](./as_field_add_in/#default) | Cast Field to [FieldAddIn](../fieldaddin/). |
|[ as_field_address_block()](./as_field_address_block/#default) | Cast Field to [FieldAddressBlock](../fieldaddressblock/). |
|[ as_field_advance()](./as_field_advance/#default) | Cast Field to [FieldAdvance](../fieldadvance/). |
|[ as_field_ask()](./as_field_ask/#default) | Cast Field to [FieldAsk](../fieldask/). |
|[ as_field_author()](./as_field_author/#default) | Cast Field to [FieldAuthor](../fieldauthor/). |
|[ as_field_auto_num()](./as_field_auto_num/#default) | Cast Field to [FieldAutoNum](../fieldautonum/). |
|[ as_field_auto_num_lgl()](./as_field_auto_num_lgl/#default) | Cast Field to [FieldAutoNumLgl](../fieldautonumlgl/). |
|[ as_field_auto_num_out()](./as_field_auto_num_out/#default) | Cast Field to [FieldAutoNumOut](../fieldautonumout/). |
|[ as_field_auto_text()](./as_field_auto_text/#default) | Cast Field to [FieldAutoText](../fieldautotext/). |
|[ as_field_auto_text_list()](./as_field_auto_text_list/#default) | Cast Field to [FieldAutoTextList](../fieldautotextlist/). |
|[ as_field_barcode()](./as_field_barcode/#default) | Cast Field to [FieldBarcode](../fieldbarcode/). |
|[ as_field_bibliography()](./as_field_bibliography/#default) | Cast Field to [FieldBibliography](../fieldbibliography/). |
|[ as_field_bidi_outline()](./as_field_bidi_outline/#default) | Cast Field to [FieldBidiOutline](../fieldbidioutline/). |
|[ as_field_citation()](./as_field_citation/#default) | Cast Field to [FieldCitation](../fieldcitation/). |
|[ as_field_comments()](./as_field_comments/#default) | Cast Field to [FieldComments](../fieldcomments/). |
|[ as_field_compare()](./as_field_compare/#default) | Cast Field to [FieldCompare](../fieldcompare/). |
|[ as_field_create_date()](./as_field_create_date/#default) | Cast Field to [FieldCreateDate](../fieldcreatedate/). |
|[ as_field_data()](./as_field_data/#default) | Cast Field to [FieldData](../fielddata/). |
|[ as_field_database()](./as_field_database/#default) | Cast Field to [FieldDatabase](../fielddatabase/). |
|[ as_field_date()](./as_field_date/#default) | Cast Field to [FieldDate](../fielddate/). |
|[ as_field_dde()](./as_field_dde/#default) | Cast Field to [FieldDde](../fielddde/). |
|[ as_field_dde_auto()](./as_field_dde_auto/#default) | Cast Field to [FieldDdeAuto](../fieldddeauto/). |
|[ as_field_display_barcode()](./as_field_display_barcode/#default) | Cast Field to [FieldDisplayBarcode](../fielddisplaybarcode/). |
|[ as_field_doc_property()](./as_field_doc_property/#default) | Cast Field to [FieldDocProperty](../fielddocproperty/). |
|[ as_field_doc_variable()](./as_field_doc_variable/#default) | Cast Field to [FieldDocVariable](../fielddocvariable/). |
|[ as_field_edit_time()](./as_field_edit_time/#default) | Cast Field to [FieldEditTime](../fieldedittime/). |
|[ as_field_embed()](./as_field_embed/#default) | Cast Field to [FieldEmbed](../fieldembed/). |
|[ as_field_eq()](./as_field_eq/#default) | Cast Field to [FieldEQ](../fieldeq/). |
|[ as_field_file_name()](./as_field_file_name/#default) | Cast Field to [FieldFileName](../fieldfilename/). |
|[ as_field_file_size()](./as_field_file_size/#default) | Cast Field to [FieldFileSize](../fieldfilesize/). |
|[ as_field_fill_in()](./as_field_fill_in/#default) | Cast Field to [FieldFillIn](../fieldfillin/). |
|[ as_field_footnote_ref()](./as_field_footnote_ref/#default) | Cast Field to [FieldFootnoteRef](../fieldfootnoteref/). |
|[ as_field_form_check_box()](./as_field_form_check_box/#default) | Cast Field to [FieldFormCheckBox](../fieldformcheckbox/). |
|[ as_field_form_drop_down()](./as_field_form_drop_down/#default) | Cast Field to [FieldFormDropDown](../fieldformdropdown/). |
|[ as_field_form_text()](./as_field_form_text/#default) | Cast Field to [FieldFormText](../fieldformtext/). |
|[ as_field_formula()](./as_field_formula/#default) | Cast Field to [FieldFormula](../fieldformula/). |
|[ as_field_glossary()](./as_field_glossary/#default) | Cast Field to [FieldGlossary](../fieldglossary/). |
|[ as_field_go_to_button()](./as_field_go_to_button/#default) | Cast Field to [FieldGoToButton](../fieldgotobutton/). |
|[ as_field_greeting_line()](./as_field_greeting_line/#default) | Cast Field to [FieldGreetingLine](../fieldgreetingline/). |
|[ as_field_hyperlink()](./as_field_hyperlink/#default) | Cast Field to [FieldHyperlink](../fieldhyperlink/). |
|[ as_field_if()](./as_field_if/#default) | Cast Field to [FieldIf](../fieldif/). |
|[ as_field_import()](./as_field_import/#default) | Cast Field to [FieldImport](../fieldimport/). |
|[ as_field_include()](./as_field_include/#default) | Cast Field to [FieldInclude](../fieldinclude/). |
|[ as_field_include_picture()](./as_field_include_picture/#default) | Cast Field to [FieldIncludePicture](../fieldincludepicture/). |
|[ as_field_include_text()](./as_field_include_text/#default) | Cast Field to [FieldIncludeText](../fieldincludetext/). |
|[ as_field_index()](./as_field_index/#default) | Cast Field to [FieldIndex](../fieldindex/). |
|[ as_field_info()](./as_field_info/#default) | Cast Field to [FieldInfo](../fieldinfo/). |
|[ as_field_keywords()](./as_field_keywords/#default) | Cast Field to [FieldKeywords](../fieldkeywords/). |
|[ as_field_last_saved_by()](./as_field_last_saved_by/#default) | Cast Field to [FieldLastSavedBy](../fieldlastsavedby/). |
|[ as_field_link()](./as_field_link/#default) | Cast Field to [FieldLink](../fieldlink/). |
|[ as_field_list_num()](./as_field_list_num/#default) | Cast Field to [FieldListNum](../fieldlistnum/). |
|[ as_field_macro_button()](./as_field_macro_button/#default) | Cast Field to [FieldMacroButton](../fieldmacrobutton/). |
|[ as_field_merge_barcode()](./as_field_merge_barcode/#default) | Cast Field to [FieldMergeBarcode](../fieldmergebarcode/). |
|[ as_field_merge_field()](./as_field_merge_field/#default) | Cast Field to [FieldMergeField](../fieldmergefield/). |
|[ as_field_merge_rec()](./as_field_merge_rec/#default) | Cast Field to [FieldMergeRec](../fieldmergerec/). |
|[ as_field_merge_seq()](./as_field_merge_seq/#default) | Cast Field to [FieldMergeSeq](../fieldmergeseq/). |
|[ as_field_next()](./as_field_next/#default) | Cast Field to [FieldNext](../fieldnext/). |
|[ as_field_next_if()](./as_field_next_if/#default) | Cast Field to [FieldNextIf](../fieldnextif/). |
|[ as_field_note_ref()](./as_field_note_ref/#default) | Cast Field to [FieldNoteRef](../fieldnoteref/). |
|[ as_field_num_chars()](./as_field_num_chars/#default) | Cast Field to [FieldNumChars](../fieldnumchars/). |
|[ as_field_num_pages()](./as_field_num_pages/#default) | Cast Field to [FieldNumPages](../fieldnumpages/). |
|[ as_field_num_words()](./as_field_num_words/#default) | Cast Field to [FieldNumWords](../fieldnumwords/). |
|[ as_field_ocx()](./as_field_ocx/#default) | Cast Field to [FieldOcx](../fieldocx/). |
|[ as_field_page()](./as_field_page/#default) | Cast Field to [FieldPage](../fieldpage/). |
|[ as_field_page_ref()](./as_field_page_ref/#default) | Cast Field to [FieldPageRef](../fieldpageref/). |
|[ as_field_print()](./as_field_print/#default) | Cast Field to [FieldPrint](../fieldprint/). |
|[ as_field_print_date()](./as_field_print_date/#default) | Cast Field to [FieldPrintDate](../fieldprintdate/). |
|[ as_field_private()](./as_field_private/#default) | Cast Field to [FieldPrivate](../fieldprivate/). |
|[ as_field_quote()](./as_field_quote/#default) | Cast Field to [FieldQuote](../fieldquote/). |
|[ as_field_rd()](./as_field_rd/#default) | Cast Field to [FieldRD](../fieldrd/). |
|[ as_field_ref()](./as_field_ref/#default) | Cast Field to [FieldRef](../fieldref/). |
|[ as_field_rev_num()](./as_field_rev_num/#default) | Cast Field to [FieldRevNum](../fieldrevnum/). |
|[ as_field_save_date()](./as_field_save_date/#default) | Cast Field to [FieldSaveDate](../fieldsavedate/). |
|[ as_field_section()](./as_field_section/#default) | Cast Field to [FieldSection](../fieldsection/). |
|[ as_field_section_pages()](./as_field_section_pages/#default) | Cast Field to [FieldSectionPages](../fieldsectionpages/). |
|[ as_field_seq()](./as_field_seq/#default) | Cast Field to [FieldSeq](../fieldseq/). |
|[ as_field_set()](./as_field_set/#default) | Cast Field to [FieldSet](../fieldset/). |
|[ as_field_shape()](./as_field_shape/#default) | Cast Field to [FieldShape](../fieldshape/). |
|[ as_field_skip_if()](./as_field_skip_if/#default) | Cast Field to [FieldSkipIf](../fieldskipif/). |
|[ as_field_style_ref()](./as_field_style_ref/#default) | Cast Field to [FieldStyleRef](../fieldstyleref/). |
|[ as_field_subject()](./as_field_subject/#default) | Cast Field to [FieldSubject](../fieldsubject/). |
|[ as_field_symbol()](./as_field_symbol/#default) | Cast Field to [FieldSymbol](../fieldsymbol/). |
|[ as_field_ta()](./as_field_ta/#default) | Cast Field to [FieldTA](../fieldta/). |
|[ as_field_tc()](./as_field_tc/#default) | Cast Field to [FieldTC](../fieldtc/). |
|[ as_field_template()](./as_field_template/#default) | Cast Field to [FieldTemplate](../fieldtemplate/). |
|[ as_field_time()](./as_field_time/#default) | Cast Field to [FieldTime](../fieldtime/). |
|[ as_field_title()](./as_field_title/#default) | Cast Field to [FieldTitle](../fieldtitle/). |
|[ as_field_toa()](./as_field_toa/#default) | Cast Field to [FieldToa](../fieldtoa/). |
|[ as_field_toc()](./as_field_toc/#default) | Cast Field to [FieldToc](../fieldtoc/). |
|[ as_field_unknown()](./as_field_unknown/#default) | Cast Field to [FieldUnknown](../fieldunknown/). |
|[ as_field_user_address()](./as_field_user_address/#default) | Cast Field to [FieldUserAddress](../fielduseraddress/). |
|[ as_field_user_initials()](./as_field_user_initials/#default) | Cast Field to [FieldUserInitials](../fielduserinitials/). |
|[ as_field_user_name()](./as_field_user_name/#default) | Cast Field to [FieldUserName](../fieldusername/). |
|[ as_field_xe()](./as_field_xe/#default) | Cast Field to [FieldXE](../fieldxe/). |
|[ get_field_code()](./get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
|[ get_field_code(include_child_field_codes)](./get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator). |
|[ remove()](./remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``. |
|[ unlink()](./unlink/#default) | Performs the field unlink. |
|[ update()](./update/#default) | Performs the field update. Throws if the field is being updated already. |
|[ update(ignore_merge_format)](./update/#bool) | Performs a field update. Throws if the field is being updated already. |

### Examples

Shows how to insert a field into a document using a field code.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
field = builder.insert_field('DATE \\@ "dddd, MMMM dd, yyyy"')
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.type)
self.assertEqual('DATE \\@ "dddd, MMMM dd, yyyy"', field.get_field_code())
# This overload of the "insert_field" method automatically updates inserted fields.
self.assertAlmostEqual(datetime.datetime.strptime(field.result, '%A, %B %d, %Y'), datetime.datetime.now(), delta=timedelta(1))
```

### See Also

* module [aspose.words.fields](../)


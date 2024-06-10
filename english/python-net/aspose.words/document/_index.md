---
title: Document class
linktitle: Document class
articleTitle: Document class
second_title: Aspose.Words for Python
description: "aspose.words.Document class. Represents a Word document"
type: docs
weight: 280
url: /python-net/aspose.words/document/
---

## Document class

Represents a Word document.
To learn more, visit the [Working with Document](https://docs.aspose.com/words/python-net/working-with-document/) documentation article.




### Remarks

The **Document** is a central object in the Aspose.Words library.

To load an existing document in any of the [LoadFormat](../loadformat/) formats, pass a file name
or a stream into one of the **Document** constructors. To create a blank document, call the
constructor without parameters.

Use one of the Save method overloads to save the document in any of the
[SaveFormat](../saveformat/) formats.

[Document.mail_merge](./mail_merge/) is the Aspose.Words's reporting engine that allows to populate
reports designed in Microsoft Word with data from various data sources quickly and easily.

**Document** stores document-wide information such as [DocumentBase.styles](../documentbase/styles/),
[Document.built_in_document_properties](./built_in_document_properties/), [Document.custom_document_properties](./custom_document_properties/), lists and macros.
Most of these objects are accessible via the corresponding properties of the **Document**.

The **Document** is a root node of a tree that contains all other nodes of the document.
The tree is a Composite design pattern and in many ways similar to XmlDocument.
The content of the document can be manipulated freely programmatically:


* The nodes of the document can be accessed via typed collections, for example [Document.sections](./sections/),
  [ParagraphCollection](../paragraphcollection/) etc.
  
* The nodes of the document can be selected by their node type using
  [CompositeNode.get_child_nodes()](../compositenode/get_child_nodes/#nodetype_bool)
  or using an XPath query with [CompositeNode.select_nodes()](../compositenode/select_nodes/#str) or [CompositeNode.select_single_node()](../compositenode/select_single_node/#str).
  
* Content nodes can be added or removed from anywhere in the document using
  [CompositeNode.insert_before()](../compositenode/insert_before/#node_node), [CompositeNode.insert_after()](../compositenode/insert_after/#node_node),
  [CompositeNode.remove_child()](../compositenode/remove_child/#node) and other
  methods provided by the base class [CompositeNode](../compositenode/).
  
* The formatting attributes of each node can be changed via the properties of that node.
  
Consider using [DocumentBuilder](../documentbuilder/) that simplifies the task of programmatically creating
or populating the document tree.

The **Document** can contain only [Section](../section/) objects.

In Microsoft Word, a valid document needs to have at least one section.




**Inheritance:** [Document](./) → [DocumentBase](../documentbase/) → [CompositeNode](../compositenode/) → [Node](../node/)

### Constructors
| Name | Description |
| --- | --- |
| [Document()](./__init__/#default) | Creates a blank Word document. |
| [Document(file_name)](./__init__/#str) | Opens an existing document from a file. Automatically detects the file format. |
| [Document(file_name, load_options)](./__init__/#str_loadoptions) | Opens an existing document from a file. Allows to specify additional options such as an encryption password. |
| [Document(stream)](./__init__/#bytesio) | Opens an existing document from a stream. Automatically detects the file format. |
| [Document(stream, load_options)](./__init__/#bytesio_loadoptions) | Opens an existing document from a stream. Allows to specify additional options such as an encryption password. |

### Properties

| Name | Description |
| --- | --- |
| [attached_template](./attached_template/) | Gets or sets the full path of the template attached to the document. |
| [automatically_update_styles](./automatically_update_styles/) | Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word. |
| [background_shape](../documentbase/background_shape/) | Gets or sets the background shape of the document. Can be ``None``.<br>(Inherited from [DocumentBase](../documentbase/)) |
| [bibliography](./bibliography/) | Gets the [Document.bibliography](./bibliography/) object that represents the list of sources available in the document. |
| [built_in_document_properties](./built_in_document_properties/) | Returns a collection that represents all the built-in document properties of the document. |
| [compatibility_options](./compatibility_options/) | Provides access to document compatibility options (that is, the user preferences entered on the **Compatibility** tab of the **Options** dialog in Word). |
| [compliance](./compliance/) | Gets the OOXML compliance version determined from the loaded document content. Makes sense only for OOXML documents. |
| [count](../compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [custom_document_properties](./custom_document_properties/) | Returns a collection that represents all the custom document properties of the document. |
| [custom_node_id](../node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [custom_xml_parts](./custom_xml_parts/) | Gets or sets the collection of Custom XML Data Storage Parts. |
| [default_tab_stop](./default_tab_stop/) | Gets or sets the interval (in points) between the default tab stops. |
| [digital_signatures](./digital_signatures/) | Gets the collection of digital signatures for this document and their validation results. |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [endnote_options](./endnote_options/) | Provides options that control numbering and positioning of endnotes in this document. |
| [field_options](./field_options/) | Gets a [FieldOptions](../../aspose.words.fields/fieldoptions/) object that represents options to control field handling in the document. |
| [first_child](../compositenode/first_child/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [first_section](./first_section/) | Gets the first section in the document. |
| [font_infos](../documentbase/font_infos/) | Provides access to properties of fonts used in this document.<br>(Inherited from [DocumentBase](../documentbase/)) |
| [font_settings](./font_settings/) | Gets or sets document font settings. |
| [footnote_options](./footnote_options/) | Provides options that control numbering and positioning of footnotes in this document. |
| [frameset](./frameset/) | Returns a [Document.frameset](./frameset/) instance if this document represents a frames page. |
| [glossary_document](./glossary_document/) | Gets or sets the glossary document within this document or template. A glossary document is a storage for AutoText, AutoCorrect and Building Block entries defined in a document. |
| [grammar_checked](./grammar_checked/) | Returns ``True`` if the document has been checked for grammar. |
| [has_child_nodes](../compositenode/has_child_nodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [has_macros](./has_macros/) | Returns ``True`` if the document has a VBA project (macros). |
| [has_revisions](./has_revisions/) | Returns ``True`` if the document has any tracked changes. |
| [hyphenation_options](./hyphenation_options/) | Provides access to document hyphenation options. |
| [include_textboxes_footnotes_endnotes_in_stat](./include_textboxes_footnotes_endnotes_in_stat/) | Specifies whether to include textboxes, footnotes and endnotes in word count statistics. |
| [is_composite](../node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [justification_mode](./justification_mode/) | Gets or sets the character spacing adjustment of a document. |
| [last_child](../compositenode/last_child/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [last_section](./last_section/) | Gets the last section in the document. |
| [layout_options](./layout_options/) | Gets a [LayoutOptions](../../aspose.words.layout/layoutoptions/) object that represents options to control the layout process of this document. |
| [lists](../documentbase/lists/) | Provides access to the list formatting used in the document.<br>(Inherited from [DocumentBase](../documentbase/)) |
| [mail_merge](./mail_merge/) | Returns a [MailMerge](../../aspose.words.mailmerging/mailmerge/) object that represents the mail merge functionality for the document. |
| [mail_merge_settings](./mail_merge_settings/) | Gets or sets the object that contains all of the mail merge information for a document. |
| [next_sibling](../node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [node_type](./node_type/) | Returns [NodeType.DOCUMENT](../nodetype/#DOCUMENT). |
| [original_file_name](./original_file_name/) | Gets the original file name of the document. |
| [original_load_format](./original_load_format/) | Gets the format of the original document that was loaded into this object. |
| [package_custom_parts](./package_custom_parts/) | Gets or sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships". |
| [page_color](../documentbase/page_color/) | Gets or sets the page color of the document. This property is a simpler version of [DocumentBase.background_shape](../documentbase/background_shape/).<br>(Inherited from [DocumentBase](../documentbase/)) |
| [page_count](./page_count/) | Gets the number of pages in the document as calculated by the most recent page layout operation. |
| [parent_node](../node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [previous_sibling](../node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [protection_type](./protection_type/) | Gets the currently active document protection type. |
| [punctuation_kerning](./punctuation_kerning/) | Specifies whether kerning applies to both Latin text and punctuation. |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |
| [remove_personal_information](./remove_personal_information/) | Gets or sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document. |
| [revisions](./revisions/) | Gets a collection of revisions (tracked changes) that exist in this document. |
| [revisions_view](./revisions_view/) | Gets or sets a value indicating whether to work with the original or revised version of a document. |
| [sections](./sections/) | Returns a collection that represents all sections in the document. |
| [shade_form_data](./shade_form_data/) | Specifies whether to turn on the gray shading on form fields. |
| [show_grammatical_errors](./show_grammatical_errors/) | Specifies whether to display grammar errors in this document. |
| [show_spelling_errors](./show_spelling_errors/) | Specifies whether to display spelling errors in this document. |
| [spelling_checked](./spelling_checked/) | Returns ``True`` if the document has been checked for spelling. |
| [styles](../documentbase/styles/) | Returns a collection of styles defined in the document.<br>(Inherited from [DocumentBase](../documentbase/)) |
| [theme](./theme/) | Gets the [Document.theme](./theme/) object for this document. |
| [track_revisions](./track_revisions/) | True if changes are tracked when this document is edited in Microsoft Word. |
| [variables](./variables/) | Returns the collection of variables added to a document or template. |
| [vba_project](./vba_project/) | Gets or sets a [Document.vba_project](./vba_project/). |
| [versions_count](./versions_count/) | Gets the number of document versions that was stored in the DOC document. |
| [view_options](./view_options/) | Provides options to control how the document is displayed in Microsoft Word. |
| [warning_callback](../documentbase/warning_callback/) | Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss.<br>(Inherited from [DocumentBase](../documentbase/)) |
| [watermark](./watermark/) | Provides access to the document watermark. |
| [web_extension_task_panes](./web_extension_task_panes/) | Returns a collection that represents a list of task pane add-ins. |
| [write_protection](./write_protection/) | Provides access to the document write protection options. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ accept_all_revisions()](./accept_all_revisions/#default) | Accepts all tracked changes in the document. |
|[ accept_end(visitor)](./accept_end/#documentvisitor) | Accepts a visitor for visiting the end of the document. |
|[ accept_start(visitor)](./accept_start/#documentvisitor) | Accepts a visitor for visiting the start of the document. |
|[ append_child(new_child)](../compositenode/append_child/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ append_document(src_doc, import_format_mode)](./append_document/#document_importformatmode) | Appends the specified document to the end of this document. |
|[ append_document(src_doc, import_format_mode, import_format_options)](./append_document/#document_importformatmode_importformatoptions) | Appends the specified document to the end of this document. |
|[ cleanup()](./cleanup/#default) | Cleans unused styles and lists from the document. |
|[ cleanup(options)](./cleanup/#cleanupoptions) | Cleans unused styles and lists from the document depending on given [CleanupOptions](../cleanupoptions/). |
|[ clone()](./clone/#default) | Performs a deep copy of the [Document](./). |
|[ clone(is_clone_children)](./clone/#bool) | Performs a deep copy of the [Document](./). |
|[ compare(document, author, date_time)](./compare/#document_str_datetime) | Compares this document with another document producing changes as number of edit and format revisions [Revision](../revision/). |
|[ compare(document, author, date_time, options)](./compare/#document_str_datetime_compareoptions) | Compares this document with another document producing changes as a number of edit and format revisions [Revision](../revision/). Allows to specify comparison options using [CompareOptions](../../aspose.words.comparing/compareoptions/). |
|[ copy_styles_from_template(template)](./copy_styles_from_template/#str) | Copies styles from the specified template to a document. |
|[ copy_styles_from_template(template)](./copy_styles_from_template/#document) | Copies styles from the specified template to a document. |
|[ ensure_minimum()](./ensure_minimum/#default) | If the document contains no sections, creates one section with one paragraph. |
|[ expand_table_styles_to_direct_formatting()](./expand_table_styles_to_direct_formatting/#default) | Converts formatting specified in table styles into direct formatting on tables in the document. |
|[ extract_pages(index, count)](./extract_pages/#int_int) | Returns the [Document](./) object representing specified range of pages. |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#object) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../node/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ get_child(node_type, index, is_deep)](../compositenode/get_child/#nodetype_int_bool) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ get_child_nodes(node_type, is_deep)](../compositenode/get_child_nodes/#nodetype_bool) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ get_page_info(page_index)](./get_page_info/#int) | Gets the page size, orientation and other information about a page that might be useful for printing or rendering. |
|[ get_text()](../node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../node/)) |
|[ import_node(src_node, is_import_children)](../documentbase/import_node/#node_bool) | Imports a node from another document to the current document.<br>(Inherited from [DocumentBase](../documentbase/)) |
|[ import_node(src_node, is_import_children, import_format_mode)](../documentbase/import_node/#node_bool_importformatmode) | Imports a node from another document to the current document with an option to control formatting.<br>(Inherited from [DocumentBase](../documentbase/)) |
|[ index_of(child)](../compositenode/index_of/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insert_after(new_child, ref_child)](../compositenode/insert_after/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insert_before(new_child, ref_child)](../compositenode/insert_before/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ join_runs_with_same_formatting()](./join_runs_with_same_formatting/#default) | Joins runs with same formatting in all paragraphs of the document. |
|[ next_pre_order(root_node)](../node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ node_type_to_string(node_type)](../node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../node/)) |
|[ normalize_field_types()](./normalize_field_types/#default) | Changes field type values [FieldChar.field_type](../../aspose.words.fields/fieldchar/field_type/) of [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/) in the whole document so that they correspond to the field types contained in the field codes. |
|[ prepend_child(new_child)](../compositenode/prepend_child/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ previous_pre_order(root_node)](../node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ protect(type)](./protect/#protectiontype) | Protects the document from changes without changing the existing password or assigns a random password. |
|[ protect(type, password)](./protect/#protectiontype_str) | Protects the document from changes and optionally sets a protection password. |
|[ remove()](../node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../node/)) |
|[ remove_all_children()](../compositenode/remove_all_children/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ remove_blank_pages()](./remove_blank_pages/#default) | Removes blank pages from the document. |
|[ remove_child(old_child)](../compositenode/remove_child/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ remove_external_schema_references()](./remove_external_schema_references/#default) | Removes external XML schema references from this document. |
|[ remove_macros()](./remove_macros/#default) | Removes all macros (the VBA project) as well as toolbars and command customizations from the document. |
|[ remove_smart_tags()](../compositenode/remove_smart_tags/#default) | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ save(file_name)](./save/#str) | Saves the document to a file. Automatically determines the save format from the extension. |
|[ save(file_name, save_format)](./save/#str_saveformat) | Saves the document to a file in the specified format. |
|[ save(file_name, save_options)](./save/#str_saveoptions) | Saves the document to a file using the specified save options. |
|[ save(stream, save_format)](./save/#bytesio_saveformat) | Saves the document to a stream using the specified format. |
|[ save(stream, save_options)](./save/#bytesio_saveoptions) | Saves the document to a stream using the specified save options. |
|[ select_nodes(xpath)](../compositenode/select_nodes/#str) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ select_single_node(xpath)](../compositenode/select_single_node/#str) | Selects the first [Node](../node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ start_track_revisions(author, date_time)](./start_track_revisions/#str_datetime) | Starts automatically marking all further changes you make to the document programmatically as revision changes. |
|[ start_track_revisions(author)](./start_track_revisions/#str) | Starts automatically marking all further changes you make to the document programmatically as revision changes. |
|[ stop_track_revisions()](./stop_track_revisions/#default) | Stops automatic marking of document changes as revisions. |
|[ to_string(save_format)](../node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ to_string(save_options)](../node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |
|[ unlink_fields()](./unlink_fields/#default) | Unlinks fields in the whole document. |
|[ unprotect()](./unprotect/#default) | Removes protection from the document regardless of the password. |
|[ unprotect(password)](./unprotect/#str) | Removes protection from the document if a correct password is specified. |
|[ update_actual_reference_marks()](./update_actual_reference_marks/#default) | Updates the [Footnote.actual_reference_mark](../../aspose.words.notes/footnote/actual_reference_mark/) property of all footnotes and endnotes in the document. |
|[ update_fields()](./update_fields/#default) | Updates the values of fields in the whole document. |
|[ update_list_labels()](./update_list_labels/#default) | Updates list labels for all list items in the document. |
|[ update_page_layout()](./update_page_layout/#default) | Rebuilds the page layout of the document. |
|[ update_table_layout()](./update_table_layout/#default) | Implements an earlier approach to table column widths re-calculation that has known issues. |
|[ update_thumbnail(options)](./update_thumbnail/#thumbnailgeneratingoptions) | Updates [BuiltInDocumentProperties.thumbnail](../../aspose.words.properties/builtindocumentproperties/thumbnail/) of the document according to the specified options. |
|[ update_thumbnail()](./update_thumbnail/#default) | Updates [BuiltInDocumentProperties.thumbnail](../../aspose.words.properties/builtindocumentproperties/thumbnail/) of the document using default options. |
|[ update_word_count()](./update_word_count/#default) | Updates word count properties of the document. |
|[ update_word_count(update_lines_count)](./update_word_count/#bool) | Updates word count properties of the document, optionally updates [BuiltInDocumentProperties.lines](../../aspose.words.properties/builtindocumentproperties/lines/) property. |

### See Also

* module [aspose.words](../)
* class [DocumentBase](../documentbase/)


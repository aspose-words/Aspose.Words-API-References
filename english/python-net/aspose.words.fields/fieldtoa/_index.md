---
title: FieldToa class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the TOA field."
type: docs
weight: 1060
url: /python-net/aspose.words.fields/fieldtoa/
---

## FieldToa class

Implements the TOA field.


Builds a table of authorities (that is, a list of the references in a legal document, such as references
to cases, statutes, and rules, along with the numbers of the pages on which the references appear) using the
entries specified by TA fields.


**Inheritance:** [FieldToa](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldToa()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets the name of the bookmark that marks the portion of the document used to build the table. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [entry_category](./entry_category/) | Gets or sets the integral category for entries included in the table. |
| [entry_separator](./entry_separator/) | Gets or sets the character sequence that is used to separate a table of authorities entry and its page number. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [page_number_list_separator](./page_number_list_separator/) | Gets or sets the character sequence that is used to separate two page numbers in a page number list. |
| [page_range_separator](./page_range_separator/) | Gets or sets the character sequence that is used to separate the start and end of a page range. |
| [remove_entry_formatting](./remove_entry_formatting/) | Gets or sets whether to remove the formatting of the entry text in the document from the entry in the table of authorities. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be null.<br>(Inherited from [Field](../field/)) |
| [sequence_name](./sequence_name/) | Gets or sets the name of a sequence whose number is included with the page number. |
| [sequence_separator](./sequence_separator/) | Gets or sets the character sequence that is used to separate sequence numbers and page numbers. |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |
| [use_heading](./use_heading/) | Gets or sets whether to include the category heading for the entries in a table of authorities. |
| [use_passim](./use_passim/) | Gets or sets whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited. |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

### Examples

Shows how to build and customize a table of authorities using TOA and TA fields.

```python
def test_field_toa(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    # Insert a TOA field, which will create an entry for each TA field in the document,
    # displaying long citations and page numbers for each entry.
    field_toa = builder.insert_field(aw.fields.FieldType.FIELD_TOA, False).as_field_toa()

    # Set the entry category for our table. This TOA will now only include TA fields
    # that have a matching value in their "entry_category" property.
    field_toa.entry_category = "1"

    # Moreover, the Table of Authorities category at index 1 is "Cases",
    # which will show up as our table's title if we set this variable to True.
    field_toa.use_heading = True

    # We can further filter TA fields by naming a bookmark that they will need to be within the TOA bounds.
    field_toa.bookmark_name = "MyBookmark"

    # By default, a dotted line page-wide tab appears between the TA field's citation
    # and its page number. We can replace it with any text we put on this property.
    # Inserting a tab character will preserve the original tab.
    field_toa.entry_separator = " \t p."

    # If we have multiple TA entries that share the same long citation,
    # all their respective page numbers will show up on one row.
    # We can use this property to specify a string that will separate their page numbers.
    field_toa.page_number_list_separator = " & p. "

    # We can set this to True to get our table to display the word "passim"
    # if there are five or more page numbers in one row.
    field_toa.use_passim = True

    # One TA field can refer to a range of pages.
    # We can specify a string here to appear between the start and end page numbers for such ranges.
    field_toa.page_range_separator = " to "

    # The format from the TA fields will carry over into our table.
    # We can disable this by setting the "remove_entry_formatting" flag.
    field_toa.remove_entry_formatting = True
    builder.font.color = drawing.Color.green
    builder.font.name = "Arial Black"

    self.assertEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", field_toa.get_field_code())

    builder.insert_break(aw.BreakType.PAGE_BREAK)

    # This TA field will not appear as an entry in the TOA since it is outside
    # the bookmark's bounds that the TOA's "bookmark_name" property specifies.
    field_ta = ExField.insert_toa_entry(builder, "1", "Source 1")

    self.assertEqual(" TA  \\c 1 \\l \"Source 1\"", field_ta.get_field_code())

    # This TA field is inside the bookmark,
    # but the entry category does not match that of the table, so the TA field will not include it.
    builder.start_bookmark("MyBookmark")
    field_ta = ExField.insert_toa_entry(builder, "2", "Source 2")

    # This entry will appear in the table.
    field_ta = ExField.insert_toa_entry(builder, "1", "Source 3")

    # A TOA table does not display short citations,
    # but we can use them as a shorthand to refer to bulky source names that multiple TA fields reference.
    field_ta.short_citation = "S.3"

    self.assertEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", field_ta.get_field_code())

    # We can format the page number to make it bold/italic using the following properties.
    # We will still see these effects if we set our table to ignore formatting.
    field_ta = ExField.insert_toa_entry(builder, "1", "Source 2")
    field_ta.is_bold = True
    field_ta.is_italic = True

    self.assertEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", field_ta.get_field_code())

    # We can configure TA fields to get their TOA entries to refer to a range of pages that a bookmark spans across.
    # Note that this entry refers to the same source as the one above to share one row in our table.
    # This row will have the page number of the entry above and the page range of this entry,
    # with the table's page list and page number range separators between page numbers.
    field_ta = ExField.insert_toa_entry(builder, "1", "Source 3")
    field_ta.page_range_bookmark_name = "MyMultiPageBookmark"

    builder.start_bookmark("MyMultiPageBookmark")
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    builder.end_bookmark("MyMultiPageBookmark")

    self.assertEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", field_ta.get_field_code())

    # If we have enabled the "Passim" feature of our table, having 5 or more TA entries with the same source will invoke it.
    for i in range(5):
        ExField.insert_toa_entry(builder, "1", "Source 4")

    builder.end_bookmark("MyBookmark")

    doc.update_fields()
    doc.save(ARTIFACTS_DIR + "Field.field_toa.docx")
    self._test_field_toa(aw.Document(ARTIFACTS_DIR + "Field.field_toa.docx")) #ExSKip

@staticmethod
def insert_toa_entry(builder: aw.DocumentBuilder, entry_category: str, long_citation: str) -> aw.fields.FieldTA:

    field = builder.insert_field(aw.fields.FieldType.FIELD_TOA_ENTRY, False).as_field_ta()
    field.entry_category = entry_category
    field.long_citation = long_citation

    builder.insert_break(aw.BreakType.PAGE_BREAK)

    return field
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)


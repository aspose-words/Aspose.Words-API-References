---
title: FieldToa class
linktitle: FieldToa class
articleTitle: FieldToa class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldToa class. Implements the TOA field"
type: docs
weight: 1060
url: /sv/python-net/aspose.words.fields/fieldtoa/
---

## FieldToa class

Implements the TOA field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

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
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
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
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

### Examples

Shows how to build and customize a table of authorities using TOA and TA fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Infoga ett TOA-fält, som kommer att skapa en post för varje TA-fält i dokumentet,
# som visar långa citat och sidnummer för varje post.
field_toa = builder.insert_field(field_type=FieldType.FIELD_TOA, update_field=False).as_field_toa()
# Ställ in postkategorin för vår tabell. Detta TOA kommer nu endast att inkludera TA-fält
# som har ett matchande värde i deras EntryCategory-egenskap.
field_toa.entry_category = '1'
# Dessutom är kategorin Table of Authorities på index 1 "Cases",
# vilket kommer att visas som vår tabells titel om vi sätter denna variabel till true.
field_toa.use_heading = True
# Vi kan ytterligare filtrera TA-fält genom att namnge ett bokmärke som de måste ligga inom TOA-gränserna.
field_toa.bookmark_name = 'MyBookmark'
# Som standard visas en prickad linje över hela sidan mellan TA-fältets citat
# och dess sidnummer. Vi kan ersätta den med vilken text vi än placerar i denna egenskap.
# Att infoga ett tabulatortecken kommer att bevara den ursprungliga tabben.
field_toa.entry_separator = ' \t p.'
# Om vi har flera TA-poster som delar samma långa citat,
# kommer alla deras respektive sidnummer att visas på en rad.
# Vi kan använda den här egenskapen för att ange en sträng som kommer att separera deras sidnummer.
field_toa.page_number_list_separator = ' & p. '
# Vi kan sätta detta till true för att få vår tabell att visa ordet "passim"
# om det finns fem eller fler sidnummer i en rad.
field_toa.use_passim = True
# Ett TA-fält kan referera till ett intervall av sidor.
# Vi kan ange en sträng här som ska visas mellan start- och slutsidnummer för sådana intervall.
field_toa.page_range_separator = ' to '
# Formatet från TA-fälten kommer att överföras till vår tabell.
# Vi kan inaktivera detta genom att sätta flaggan RemoveEntryFormatting.
field_toa.remove_entry_formatting = True
builder.font.color = Color.green
builder.font.name = 'Arial Black'
self.assertEqual(' TOA  \\c 1 \\h \\b MyBookmark \\e " \t p." \\l " & p. " \\p \\g " to " \\f', field_toa.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Detta TA-fält kommer inte att visas som en post i TOA eftersom det är utanför
# bokmärkesgränserna som TOA:s egenskap BookmarkName specificerar.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 1')
self.assertEqual(' TA  \\c 1 \\l "Source 1"', field_ta.get_field_code())
# Detta TA-fält är inne i bokmärket,
# men postkategorin matchar inte tabellens, så TA-fältet kommer inte att inkludera den.
builder.start_bookmark('MyBookmark')
field_ta = ExField._insert_toa_entry(builder, '2', 'Source 2')
# Denna post kommer att visas i tabellen.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 3')
# En TOA-tabell visar inte korta citat,
# men vi kan använda dem som en förkortning för att referera till långa källnamn som flera TA-fält refererar till.
field_ta.short_citation = 'S.3'
self.assertEqual(' TA  \\c 1 \\l "Source 3" \\s S.3', field_ta.get_field_code())
# Vi kan formatera sidnumret för att göra det fetstil/kursiv med hjälp av följande egenskaper.
# Vi kommer fortfarande att se dessa effekter om vi ställer in vår tabell på att ignorera formatering.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 2')
field_ta.is_bold = True
field_ta.is_italic = True
self.assertEqual(' TA  \\c 1 \\l "Source 2" \\b \\i', field_ta.get_field_code())
# Vi kan konfigurera TA-fält för att få deras TOA-poster att referera till ett sidintervall som ett bokmärke sträcker sig över.
# Observera att denna post refererar till samma källa som den ovanför för att dela en rad i vår tabell.
# Denna rad kommer att ha sidnumret från posten ovan och sidintervallet för denna post,
# med tabellens sidlista och separatorer för sidnummerintervall mellan sidnummer.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 3')
field_ta.page_range_bookmark_name = 'MyMultiPageBookmark'
builder.start_bookmark('MyMultiPageBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.end_bookmark('MyMultiPageBookmark')
self.assertEqual(' TA  \\c 1 \\l "Source 3" \\r MyMultiPageBookmark', field_ta.get_field_code())
# Om vi har aktiverat "Passim"-funktionen i vår tabell, kommer att ha 5 eller fler TA-poster med samma källa att utlösa den.
i = 0
while i < 5:
    ExField._insert_toa_entry(builder, '1', 'Source 4')
    i += 1
builder.end_bookmark('MyBookmark')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOA.TA.docx')
```

Shows how to build and customize a table of authorities using TOA and TA fields (InsertToaEntry).

```python
@staticmethod
def _insert_toa_entry(builder, entry_category, long_citation):
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOA_ENTRY, update_field=False).as_field_ta()
    field.entry_category = entry_category
    field.long_citation = long_citation
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    return field
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)


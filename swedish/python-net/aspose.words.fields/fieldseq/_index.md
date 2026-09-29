---
title: FieldSeq class
linktitle: FieldSeq class
articleTitle: FieldSeq class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldSeq class. Implements the SEQ field"
type: docs
weight: 930
url: /sv/python-net/aspose.words.fields/fieldseq/
---

## FieldSeq class

Implements the SEQ field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Sequentially numbers chapters, tables, figures, and other user-defined lists of items in a document.


**Inheritance:** [FieldSeq](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldSeq()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [insert_next_number](./insert_next_number/) | Gets or sets whether to insert the next sequence number for the specified item. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [reset_heading_level](./reset_heading_level/) | Gets or sets an integer number representing a heading level to reset the sequence number to. Returns -1 if the number is absent. |
| [reset_number](./reset_number/) | Gets or sets an integer number to reset the sequence number to. Returns -1 if the number is absent. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [sequence_identifier](./sequence_identifier/) | Gets or sets the name assigned to the series of items that are to be numbered. |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

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

Shows how to populate a TOC field with entries using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ett TOC-fält kan skapa en post i sin innehållsförteckning för varje SEQ-fält som finns i dokumentet.
# Varje post innehåller stycket som inkluderar SEQ-fältet och sidnumret där fältet visas.
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# SEQ-fält visar ett räknare som ökas vid varje SEQ-fält.
# Dessa fält upprätthåller också separata räknare för varje unikt namngivet sekvens
# identifierad av SEQ-fältets egenskap "SequenceIdentifier".
# Använd egenskapen "TableOfFiguresLabel" för att namnge en huvudsekvens för TOC.
# Nu kommer detta TOC endast att skapa poster från SEQ-fält med deras "SequenceIdentifier" inställd på "MySequence".
field_toc.table_of_figures_label = 'MySequence'
# Vi kan namnge en annan SEQ-fältsekvens i egenskapen "PrefixedSequenceIdentifier".
# SEQ-fält från denna prefixsekvens kommer inte att skapa TOC-poster.
# Varje TOC-post som skapas från ett huvudsekvens‑SEQ-fält kommer nu också att visa räknaren som
# prefixsekvensen är för närvarande på det primära sekvens‑SEQ‑fältet som skapade posten.
field_toc.prefixed_sequence_identifier = 'PrefixSequence'
# Varje TOC‑post kommer att visa prefixsekvensens räknare omedelbart till vänster
# av sidnumret som huvudsekvensens SEQ‑fält visas på.
# Vi kan ange en anpassad avgränsare som kommer att visas mellan dessa två tal.
field_toc.sequence_separator = '>'
self.assertEqual(' TOC  \\c MySequence \\s PrefixSequence \\d >', field_toc.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Det finns två sätt att använda SEQ‑fält för att fylla i denna TOC.
# 1 -  Infoga ett SEQ‑fält som tillhör TOC:s prefixsekvens:
# Detta fält kommer att öka SEQ‑sekvensräkningen för "PrefixSequence" med 1.
# Eftersom detta fält inte tillhör den identifierade huvudsekvensen
# av TOC:s egenskap "TableOfFiguresLabel", kommer det inte att visas som en post.
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
self.assertEqual(' SEQ  PrefixSequence', field_seq.get_field_code())
# 2 -  Infoga ett SEQ‑fält som tillhör TOC:s huvudsekvens:
# Detta SEQ‑fält kommer att skapa en post i TOC.
# TOC‑posten kommer att innehålla det stycke som SEQ‑fältet finns i samt sidnumret där det visas.
# Denna post kommer också att visa räknaren som prefixsekvensen för närvarande har,
# separerad från sidnumret av värdet i TOC:s egenskap SeqenceSeparator.
# "PrefixSequence"‑räkningen är 1, detta huvudsekvens‑SEQ‑fält är på sida 2,
# och avgränsaren är ">", så posten kommer att visa "1>2".
builder.write('First TOC entry, MySequence #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', field_seq.get_field_code())
# Infoga en sida, öka prefixsekvensen med 2, och infoga ett SEQ‑fält för att därefter skapa en TOC‑post.
# Prefixsekvensen är nu 2, och huvudsekvens‑SEQ‑fältet är på sida 3,
# så TOC‑posten kommer att visa "2>3" vid dess sidräkning.
builder.insert_break(aw.BreakType.PAGE_BREAK)
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
builder.write('Second TOC entry, MySequence #')
field_seq.sequence_identifier = 'MySequence'
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOC.SEQ.docx')
```

Shows create numbering using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# SEQ-fält visar ett räknare som ökas vid varje SEQ-fält.
# Dessa fält upprätthåller också separata räknare för varje unikt namngivet sekvens
# identifierad av SEQ-fältets egenskap "SequenceIdentifier".
# Infoga ett SEQ‑fält som kommer att visa det aktuella räknarvärdet för "MySequence",
# efter att ha använt egenskapen "ResetNumber" för att sätta den till 100.
builder.write('#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_number = '100'
field_seq.update()
self.assertEqual(' SEQ  MySequence \\r 100', field_seq.get_field_code())
self.assertEqual('100', field_seq.result)
# Visa nästa nummer i denna sekvens med ett annat SEQ‑fält.
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.update()
self.assertEqual('101', field_seq.result)
# Infoga en rubrik på nivå 1.
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('This level 1 heading will reset MySequence to 1')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
# Infoga ett annat SEQ‑fält från samma sekvens och konfigurera det att återställa räknaren till 1 vid varje rubrik.
builder.write('\n#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_heading_level = '1'
field_seq.update()
# Ovanstående rubrik är en rubrik på nivå 1, så räknaren för denna sekvens återställs till 1.
self.assertEqual(' SEQ  MySequence \\s 1', field_seq.get_field_code())
self.assertEqual('1', field_seq.result)
# Gå till nästa nummer i den här sekvensen.
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.insert_next_number = True
field_seq.update()
self.assertEqual(' SEQ  MySequence \\n', field_seq.get_field_code())
self.assertEqual('2', field_seq.result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SEQ.ResetNumbering.docx')
```

Shows how to combine table of contents and sequence fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ett TOC-fält kan skapa en post i sin innehållsförteckning för varje SEQ-fält som finns i dokumentet.
# Varje post innehåller stycket som innehåller SEQ-fältet,
# och sidnumret där fältet visas.
field_toc = builder.insert_field(field_type=FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Konfigurera detta TOC-fält så att det har egenskapen SequenceIdentifier med värdet "MySequence".
field_toc.table_of_figures_label = 'MySequence'
# Konfigurera detta TOC-fält så att det bara plockar upp SEQ-fält som ligger inom gränserna för ett bokmärke
# med namnet "TOCBookmark".
field_toc.bookmark_name = 'TOCBookmark'
builder.insert_break(aw.BreakType.PAGE_BREAK)
self.assertEqual(' TOC  \\c MySequence \\b TOCBookmark', field_toc.get_field_code())
# SEQ-fält visar ett räknare som ökas vid varje SEQ-fält.
# Dessa fält upprätthåller också separata räknare för varje unikt namngivet sekvens
# identifierad av SEQ-fältets egenskap "SequenceIdentifier".
# Infoga ett SEQ-fält som har en sekvensidentifierare som matchar TOC:ens
# TableOfFiguresLabel-egenskapen. Detta fält kommer inte att skapa en post i TOC eftersom det är utanför
# bokmärkesgränserna som anges av "BookmarkName".
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will not show up in the TOC because it is outside of the bookmark.')
builder.start_bookmark('TOCBookmark')
# Detta SEQ-fälts sekvens matchar TOC:ens "TableOfFiguresLabel"-egenskap och ligger inom bokmärkesgränserna.
# Stycket som innehåller detta fält kommer att visas i TOC som en post.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will show up in the TOC next to the entry for the above caption.')
# Detta SEQ-fälts sekvens matchar inte TOC:ens "TableOfFiguresLabel"-egenskap,
# och ligger inom bokmärkesgränserna. Dess stycke kommer inte att visas i TOC som en post.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'OtherSequence'
builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.")
# Detta SEQ-fälts sekvens matchar TOC:ens "TableOfFiguresLabel"-egenskap och ligger inom bokmärkesgränserna.
# Detta fält refererar också till ett annat bokmärke. Innehållet i det bokmärket kommer att visas i TOC-posten för detta SEQ-fält.
# SEQ-fältet självt kommer inte att visa innehållet i det bokmärket.
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.bookmark_name = 'SEQBookmark'
self.assertEqual(' SEQ  MySequence SEQBookmark', field_seq.get_field_code())
# Skapa ett bokmärke med innehåll som kommer att visas i TOC-posten på grund av att ovanstående SEQ-fält refererar till det.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('SEQBookmark')
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', text from inside SEQBookmark.')
builder.end_bookmark('SEQBookmark')
builder.end_bookmark('TOCBookmark')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SEQ.Bookmark.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)


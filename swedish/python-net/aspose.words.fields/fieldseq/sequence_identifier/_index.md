---
title: FieldSeq.sequence_identifier property
linktitle: sequence_identifier property
articleTitle: sequence_identifier property
second_title: Aspose.Words for Python
description: "FieldSeq.sequence_identifier property. Gets or sets the name assigned to the series of items that are to be numbered."
type: docs
weight: 60
url: /sv/python-net/aspose.words.fields/fieldseq/sequence_identifier/
---

## FieldSeq.sequence_identifier property

Gets or sets the name assigned to the series of items that are to be numbered.


```python
@property
def sequence_identifier(self) -> str:
    ...

@sequence_identifier.setter
def sequence_identifier(self, value: str):
    ...

```

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

### See Also

* module [aspose.words.fields](../../)
* class [FieldSeq](../)


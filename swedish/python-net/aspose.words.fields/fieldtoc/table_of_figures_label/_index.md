---
title: FieldToc.table_of_figures_label property
linktitle: table_of_figures_label property
articleTitle: table_of_figures_label property
second_title: Aspose.Words for Python
description: "FieldToc.table_of_figures_label property. Gets or sets the name of the sequence identifier used when building a table of figures."
type: docs
weight: 160
url: /sv/python-net/aspose.words.fields/fieldtoc/table_of_figures_label/
---

## FieldToc.table_of_figures_label property

Gets or sets the name of the sequence identifier used when building a table of figures.


```python
@property
def table_of_figures_label(self) -> str:
    ...

@table_of_figures_label.setter
def table_of_figures_label(self, value: str):
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

### See Also

* module [aspose.words.fields](../../)
* class [FieldToc](../)


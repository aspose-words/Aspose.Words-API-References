---
title: ListLevel.restart_after_level property
linktitle: restart_after_level property
articleTitle: restart_after_level property
second_title: Aspose.Words for Python
description: "ListLevel.restart_after_level property. Sets or returns the list level that must appear before the specified list level restarts numbering."
type: docs
weight: 100
url: /it/python-net/aspose.words.lists/listlevel/restart_after_level/
---

## ListLevel.restart_after_level property

Sets or returns the list level that must appear before the specified list level restarts numbering.


```python
@property
def restart_after_level(self) -> int:
    ...

@restart_after_level.setter
def restart_after_level(self, value: int):
    ...

```

### Remarks

The value of -1 means the numbering will continue.




### Examples

Shows advances ways of customizing list labels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli prefisso e rientri.
# Possiamo creare elenchi nidificati aumentando il livello di rientro.
# Possiamo iniziare e terminare un elenco usando la proprietà \"ListFormat\" di un document builder.
# Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
# Le etichette di livello 1 saranno formattate secondo lo stile di paragrafo "Heading 1" e avranno un prefisso.
# Queste appariranno come "Appendix A", "Appendix B"...
doc_list.list_levels[0].number_format = 'Appendix \x00'
doc_list.list_levels[0].number_style = aw.NumberStyle.UPPERCASE_LETTER
doc_list.list_levels[0].linked_style = doc.styles.get_by_name('Heading 1')
# Le etichette di livello 2 mostreranno i numeri attuali del primo e del secondo livello dell'elenco e avranno zeri iniziali.
# Se il primo livello dell'elenco è a 1, allora le etichette di questi elenchi appariranno come "Section (1.01)", "Section (1.02)"...
doc_list.list_levels[1].number_format = 'Section (\x00.\x01)'
doc_list.list_levels[1].number_style = aw.NumberStyle.LEADING_ZERO
# Nota che il livello superiore utilizza la numerazione UppercaseLetter.
# Possiamo impostare la proprietà "IsLegal" per utilizzare numeri arabi nei livelli superiori dell'elenco.
doc_list.list_levels[1].is_legal = True
doc_list.list_levels[1].restart_after_level = 0
# Le etichette di livello 3 saranno numeri romani maiuscoli con un prefisso e un suffisso e si riavvieranno per ogni elemento di livello 1 dell'elenco.
# Queste etichette di elenco appariranno come "-I-", "-II-"...
doc_list.list_levels[2].number_format = '-\x02-'
doc_list.list_levels[2].number_style = aw.NumberStyle.UPPERCASE_ROMAN
doc_list.list_levels[2].restart_after_level = 1
# Rendi le etichette di tutti i livelli dell'elenco in grassetto.
for level in doc_list.list_levels:
    level.font.bold = True
# Applica la formattazione dell'elenco al paragrafo corrente.
builder.list_format.list = doc_list
# Crea gli elementi dell'elenco che visualizzeranno tutti e tre i nostri livelli di elenco.
n = 0
while n < 2:
    i = 0
    while i < 3:
        builder.list_format.list_level_number = i
        builder.writeln('Level ' + str(i))
        i += 1
    n += 1
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.CreateListRestartAfterHigher.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)


---
title: ListFormat.list_level_number property
linktitle: list_level_number property
articleTitle: list_level_number property
second_title: Aspose.Words for Python
description: "ListFormat.list_level_number property. Gets or sets the list level number (0 to 8) for the paragraph."
type: docs
weight: 40
url: /it/python-net/aspose.words.lists/listformat/list_level_number/
---

## ListFormat.list_level_number property

Gets or sets the list level number (0 to 8) for the paragraph.


```python
@property
def list_level_number(self) -> int:
    ...

@list_level_number.setter
def list_level_number(self, value: int):
    ...

```

### Remarks

In Word documents, lists may consist of 1 or 9 levels, numbered 0 to 8.

Has effect only when the [ListFormat.list](../list/) property is set to reference a valid list.




### Examples

Shows how to create bulleted and numbered lists.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Aspose.Words main advantages are:')
# Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli prefisso e rientri.
# Possiamo creare elenchi nidificati aumentando il livello di rientro.
# Possiamo iniziare e terminare un elenco usando la proprietà \"ListFormat\" di un document builder.
# Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
# Di seguito sono due tipi di elenchi che possiamo creare con un document builder.
# 1 -  Un elenco puntato:
# Questo elenco applicherà un rientro e un simbolo di punto elenco (\"•\") prima di ogni paragrafo.
builder.list_format.apply_bullet_default()
builder.writeln('Great performance')
builder.writeln('High reliability')
builder.writeln('Quality code and working')
builder.writeln('Wide variety of features')
builder.writeln('Easy to understand API')
# Termina l'elenco puntato.
builder.list_format.remove_numbers()
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.writeln('Aspose.Words allows:')
# 2 -  Un elenco numerato:
# Gli elenchi numerati creano un ordine logico per i loro paragrafi numerando ogni elemento.
builder.list_format.apply_number_default()
# Questo paragrafo è il primo elemento. Il primo elemento di un elenco numerato avrà un "1." come simbolo dell'elemento dell'elenco.
builder.writeln('Opening documents from different formats:')
self.assertEqual(0, builder.list_format.list_level_number)
# Chiama il metodo "ListIndent" per aumentare il livello di elenco corrente,
# che avvierà un nuovo elenco autonomo, con un rientro più profondo, all'elemento corrente del primo livello di elenco.
builder.list_format.list_indent()
self.assertEqual(1, builder.list_format.list_level_number)
# Questi sono i primi tre elementi dell'elenco del secondo livello, che manterranno un conteggio
# indipendente dal conteggio del primo livello di elenco. Secondo il formato di elenco corrente,
# avranno simboli "a.", "b.", e "c.".
builder.writeln('DOC')
builder.writeln('PDF')
builder.writeln('HTML')
# Chiama il metodo "ListOutdent" per tornare al livello di elenco precedente.
builder.list_format.list_outdent()
self.assertEqual(0, builder.list_format.list_level_number)
# Questi due paragrafi continueranno il conteggio del primo livello di elenco.
# Questi elementi avranno simboli "2.", e "3."
builder.writeln('Processing documents')
builder.writeln('Saving documents in different formats:')
# Se aumentiamo il livello di elenco a un livello al quale abbiamo già aggiunto elementi in precedenza,
# l'elenco annidato sarà separato dal precedente e la sua numerazione inizierà dall'inizio.
# Questi elementi dell'elenco avranno i simboli di "a.", "b.", "c.", "d.", e "e".
builder.list_format.list_indent()
builder.writeln('DOC')
builder.writeln('PDF')
builder.writeln('HTML')
builder.writeln('MHTML')
builder.writeln('Plain text')
# Rimuovi l'indentazione del livello dell'elenco di nuovo.
builder.list_format.list_outdent()
builder.writeln('Doing many other things!')
# Termina l'elenco numerato.
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.ApplyDefaultBulletsAndNumbers.docx')
```

Shows how to work with list levels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
self.assertFalse(builder.list_format.is_list_item)
# Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli prefisso e rientri.
# Possiamo creare elenchi nidificati aumentando il livello di rientro.
# Possiamo iniziare e terminare un elenco usando la proprietà \"ListFormat\" di un document builder.
# Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
# Di seguito sono riportati due tipi di elenchi che possiamo creare usando un document builder.
# 1 -  Un elenco numerato:
# Gli elenchi numerati creano un ordine logico per i loro paragrafi numerando ogni elemento.
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
self.assertTrue(builder.list_format.is_list_item)
# Impostando la proprietà \"ListLevelNumber\", possiamo aumentare il livello dell'elenco
# per avviare un sottoelenco autonomo all'elemento corrente dell'elenco.
# Il modello di elenco di Microsoft Word chiamato \"NumberDefault\" utilizza numeri per creare livelli di elenco per il primo livello.
# I livelli di elenco più profondi usano lettere e numeri romani minuscoli.
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# 2 -  Un elenco puntato:
# Questo elenco applicherà un rientro e un simbolo di punto elenco (\"•\") prima di ogni paragrafo.
# I livelli più profondi di questo elenco utilizzeranno simboli diversi, come \"■\" e \"○\".
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# Possiamo disabilitare la formattazione degli elenchi per non formattare i paragrafi successivi come elenchi rimuovendo il flag \"List\".
builder.list_format.list = None
self.assertFalse(builder.list_format.is_list_item)
doc.save(file_name=ARTIFACTS_DIR + 'Lists.SpecifyListLevel.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)
* property [ListFormat.list](../list/)


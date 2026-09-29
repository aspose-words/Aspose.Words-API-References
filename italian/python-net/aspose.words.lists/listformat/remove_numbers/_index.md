---
title: ListFormat.remove_numbers method
linktitle: remove_numbers method
articleTitle: remove_numbers method
second_title: Aspose.Words for Python
description: "ListFormat.remove_numbers method. Removes numbers or bullets from the current paragraph and sets list level to zero."
type: docs
weight: 90
url: /it/python-net/aspose.words.lists/listformat/remove_numbers/
---

## remove_numbers() {#default}

Removes numbers or bullets from the current paragraph and sets list level to zero.


```python
def remove_numbers(self):
    ...
```

### Remarks

Calling this method is equivalent to setting the [ListFormat.list](../list/) property to ``None``.




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

Shows how to remove list formatting from all paragraphs in the main text of a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.list_format.apply_number_default()
builder.writeln('Numbered list item 1')
builder.writeln('Numbered list item 2')
builder.writeln('Numbered list item 3')
builder.list_format.remove_numbers()
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
self.assertEqual(3, len(list(filter(lambda n: n.as_paragraph().list_format.is_list_item, paras))))
for paragraph in paras:
    paragraph = paragraph.as_paragraph()
    paragraph.list_format.remove_numbers()
self.assertEqual(0, len(list(filter(lambda n: n.as_paragraph().list_format.is_list_item, paras))))
```

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)


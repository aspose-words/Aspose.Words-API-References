---
title: Range.replace method
linktitle: replace method
articleTitle: replace method
second_title: Aspose.Words for Python
description: "aspose.words.Range.replace method"
type: docs
weight: 90
url: /it/python-net/aspose.words/range/replace/
---

## replace(pattern, replacement) {#str_str}

Replaces all occurrences of a specified character string pattern with a replacement string.


```python
def replace(self, pattern: str, replacement: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern | str | A string to be replaced. |
| replacement | str | A string to replace all occurrences of pattern. |

### Remarks

The pattern will not be used as regular expression.
Please use Aspose.Words.Range.Replace(System.Text.RegularExpressions.Regex,System.String) if you need regular expressions.

Used case-insensitive comparison.

Method is able to process breaks in both pattern and replacement strings.


You should use special meta-characters if you need to work with breaks:
* **&p** - paragraph break
  
* **&b** - section break
  
* **&m** - page break
  
* **&l** - manual line break
  

Use method[Range.replace()](./#str_str_findreplaceoptions) to have more flexible customization.



### Returns

The number of replacements made.


## replace(pattern, replacement, options) {#str_str_findreplaceoptions}

Replaces all occurrences of a specified character string pattern with a replacement string.


```python
def replace(self, pattern: str, replacement: str, options: aspose.words.replacing.FindReplaceOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern | str | A string to be replaced. |
| replacement | str | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

### Remarks

The pattern will not be used as regular expression.
Please use Aspose.Words.Range.Replace(System.Text.RegularExpressions.Regex,System.String,Aspose.Words.Replacing.FindReplaceOptions) if you need regular expressions.

Method is able to process breaks in both pattern and replacement strings.


You should use special meta-characters if you need to work with breaks:
* **&p** - paragraph break
  
* **&b** - section break
  
* **&m** - page break
  
* **&l** - manual line break
  
* **&&** - & character
  



### Returns

The number of replacements made.


## Examples

Shows how to perform a find-and-replace text operation on the contents of a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Greetings, _FullName_!')
# Esegui un'operazione di ricerca e sostituzione sul contenuto del nostro documento e verifica il numero di sostituzioni effettuate.
replacement_count = doc.range.replace(pattern='_FullName_', replacement='John Doe')
self.assertEqual(1, replacement_count)
self.assertEqual('Greetings, John Doe!', doc.get_text().strip())
```

Shows how to add formatting to paragraphs in which a find-and-replace operation has found matches.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Every paragraph that ends with a full stop like this one will be right aligned.')
builder.writeln('This one will not!')
builder.write('This one also will.')
paragraphs = doc.first_section.body.paragraphs
self.assertEqual(aw.ParagraphAlignment.LEFT, paragraphs[0].paragraph_format.alignment)
self.assertEqual(aw.ParagraphAlignment.LEFT, paragraphs[1].paragraph_format.alignment)
self.assertEqual(aw.ParagraphAlignment.LEFT, paragraphs[2].paragraph_format.alignment)
# Possiamo usare un oggetto \"FindReplaceOptions\" per modificare il processo di ricerca e sostituzione.
options = aw.replacing.FindReplaceOptions()
# Imposta la proprietà "Alignment" su "ParagraphAlignment.Right" per allineare a destra ogni paragrafo
# che contiene una corrispondenza trovata dall'operazione di ricerca e sostituzione.
options.apply_paragraph_format.alignment = aw.ParagraphAlignment.RIGHT
# Sostituisci ogni punto che si trova subito prima di un'interruzione di paragrafo con un punto esclamativo.
count = doc.range.replace(pattern='.&p', replacement='!&p', options=options)
self.assertEqual(2, count)
self.assertEqual(aw.ParagraphAlignment.RIGHT, paragraphs[0].paragraph_format.alignment)
self.assertEqual(aw.ParagraphAlignment.LEFT, paragraphs[1].paragraph_format.alignment)
self.assertEqual(aw.ParagraphAlignment.RIGHT, paragraphs[2].paragraph_format.alignment)
self.assertEqual('Every paragraph that ends with a full stop like this one will be right aligned!\r' + 'This one will not!\r' + 'This one also will!', doc.get_text().strip())
```

Shows how to replace text in a document's footer.

```python
doc = aw.Document(file_name=MY_DIR + 'Footer.docx')
headers_footers = doc.first_section.headers_footers
footer = headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_PRIMARY)
options = aw.replacing.FindReplaceOptions()
options.match_case = False
options.find_whole_words_only = False
current_year = datetime.datetime.now().year
footer.range.replace(pattern='(C) 2006 Aspose Pty Ltd.', replacement=f'Copyright (C) {current_year} by Aspose Pty Ltd.', options=options)
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.ReplaceText.docx')
```

Shows how to toggle case sensitivity when performing a find-and-replace operation.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Ruby bought a ruby necklace.')
# Possiamo usare un oggetto \"FindReplaceOptions\" per modificare il processo di ricerca e sostituzione.
options = aw.replacing.FindReplaceOptions()
# Imposta il flag \"MatchCase\" su \"true\" per applicare la distinzione tra maiuscole e minuscole durante la ricerca delle stringhe da sostituire.
# Imposta il flag \"MatchCase\" su \"false\" per ignorare le maiuscole/minuscole durante la ricerca del testo da sostituire.
options.match_case = match_case
doc.range.replace(pattern='Ruby', replacement='Jade', options=options)
self.assertEqual('Jade bought a ruby necklace.' if match_case else 'Jade bought a Jade necklace.', doc.get_text().strip())
```

Shows how to toggle standalone word-only find-and-replace operations.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Jackson will meet you in Jacksonville.')
# Possiamo usare un oggetto \"FindReplaceOptions\" per modificare il processo di ricerca e sostituzione.
options = aw.replacing.FindReplaceOptions()
# Imposta il flag \"FindWholeWordsOnly\" su \"true\" per sostituire il testo trovato se non è parte di un'altra parola.
# Imposta il flag \"FindWholeWordsOnly\" su \"false\" per sostituire tutto il testo indipendentemente dal contesto.
options.find_whole_words_only = find_whole_words_only
doc.range.replace(pattern='Jackson', replacement='Louis', options=options)
self.assertEqual('Louis will meet you in Jacksonville.' if find_whole_words_only else 'Louis will meet you in Louisville.', doc.get_text().strip())
```

Shows how to replace all instances of String of text in a table and cell.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Carrots')
builder.insert_cell()
builder.write('50')
builder.end_row()
builder.insert_cell()
builder.write('Potatoes')
builder.insert_cell()
builder.write('50')
builder.end_table()
options = aw.replacing.FindReplaceOptions()
options.match_case = True
options.find_whole_words_only = True
# Esegui un'operazione di ricerca e sostituzione su un'intera tabella.
table.range.replace(pattern='Carrots', replacement='Eggs', options=options)
# Esegui un'operazione di ricerca e sostituzione sull'ultima cella dell'ultima riga della tabella.
table.last_row.last_cell.range.replace(pattern='50', replacement='20', options=options)
self.assertEqual('Eggs\x0750\x07\x07' + 'Potatoes\x0720\x07\x07', table.get_text().strip())
```

## See Also

* module [aspose.words](../../)
* class [Range](../)


---
title: Document.extract_pages method
linktitle: extract_pages method
articleTitle: extract_pages method
second_title: Aspose.Words for Python
description: "aspose.words.Document.extract_pages method"
type: docs
weight: 650
url: /fr/python-net/aspose.words/document/extract_pages/
---

## extract_pages(index, count, options) {#int_int_pageextractoptions}

Returns the [Document](../) object representing the specified range of pages and the given page extract options.



```python
def extract_pages(self, index: int, count: int, options: aspose.words.PageExtractOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the first page to extract. |
| count | int | Number of pages to be extracted. |
| options | [PageExtractOptions](../../pageextractoptions/) | Provides options for managing the page extracting process. |

### Remarks

The resulting document should look like the one in MS Word, as if we had performed 'Print specific pages' – the numbering,
headers/footers and cross tables layout will be preserved.
But due to a large number of nuances, appearing while reducing the number of pages, full match of the layout is a quiet complicated task requiring a lot of effort.
Depending on the document complexity there might be slight differences in the resulting document contents layout comparing to the source document.
Any feedback would be greatly appreciated.


## extract_pages(index, count) {#int_int}

Returns the [Document](../) object representing specified range of pages.



```python
def extract_pages(self, index: int, count: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the first page to extract. |
| count | int | Number of pages to be extracted. |

### Remarks

The resulting document should look like the one in MS Word, as if we had performed 'Print specific pages' – the numbering,
headers/footers and cross tables layout will be preserved.
But due to a large number of nuances, appearing while reducing the number of pages, full match of the layout is a quiet complicated task requiring a lot of effort.
Depending on the document complexity there might be slight differences in the resulting document contents layout comparing to the source document.
Any feedback would be greatly appreciated.


## Examples

Shows how to get specified range of pages from the document.

```python
doc = aw.Document(file_name=MY_DIR + 'Layout entities.docx')
doc = doc.extract_pages(index=0, count=2)
doc.save(file_name=ARTIFACTS_DIR + 'Document.ExtractPages.docx')
```

Show how to reset the initial page numbering and save the NUMPAGE field.

```python
doc = aw.Document(file_name=MY_DIR + 'Page fields.docx')
# Comportement par défaut :
# La numérotation des pages extraite est la même que dans le document original, comme si nous avions sélectionné "Print 2 pages" dans MS Word.
# La page de départ sera définie sur 2 et le champ indiquant le nombre de pages sera supprimé
# et remplacé par une valeur constante égale au nombre de pages.
extracted_doc1 = doc.extract_pages(index=1, count=1)
extracted_doc1.save(file_name=ARTIFACTS_DIR + 'Document.ExtractPagesWithOptions.Default.docx')
# Comportement modifié :
# La numérotation des pages extraite est réinitialisée et une nouvelle commence,
# comme si nous avions copié le contenu de la deuxième page et l'avions collé dans un nouveau document.
# La page de départ sera définie sur 1 et le champ indiquant le nombre de pages restera inchangé
# et affichera le nombre actuel de pages.
extract_options = aw.PageExtractOptions()
extract_options.update_page_starting_number = False
extract_options.unlink_pages_number_fields = False
extracted_doc2 = doc.extract_pages(index=1, count=1, options=extract_options)
extracted_doc2.save(file_name=ARTIFACTS_DIR + 'Document.ExtractPagesWithOptions.Options.docx')
```

## See Also

* module [aspose.words](../../)
* class [Document](../)


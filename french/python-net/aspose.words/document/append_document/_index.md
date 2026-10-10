---
title: Document.append_document method
linktitle: append_document method
articleTitle: append_document method
second_title: Aspose.Words for Python
description: "aspose.words.Document.append_document method"
type: docs
weight: 580
url: /fr/python-net/aspose.words/document/append_document/
---

## append_document(src_doc, import_format_mode) {#document_importformatmode}

Appends the specified document to the end of this document.


```python
def append_document(self, src_doc: aspose.words.Document, import_format_mode: aspose.words.ImportFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_doc | [Document](../) | The document to append. |
| import_format_mode | [ImportFormatMode](../../importformatmode/) | Specifies how to merge style formatting that clashes. |

## append_document(src_doc, import_format_mode, import_format_options) {#document_importformatmode_importformatoptions}

Appends the specified document to the end of this document.


```python
def append_document(self, src_doc: aspose.words.Document, import_format_mode: aspose.words.ImportFormatMode, import_format_options: aspose.words.ImportFormatOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_doc | [Document](../) | The document to append. |
| import_format_mode | [ImportFormatMode](../../importformatmode/) | Specifies how to merge style formatting that clashes. |
| import_format_options | [ImportFormatOptions](../../importformatoptions/) | Allows to specify options that affect formatting of a result document. |

## Examples

Shows how to append a document to the end of another document.

```python
src_doc = aw.Document()
src_doc.first_section.body.append_paragraph('Source document text. ')
dst_doc = aw.Document()
dst_doc.first_section.body.append_paragraph('Destination document text. ')
# Ajoutez le document source au document de destination tout en préservant son formatage,
# puis enregistrez le document source sur le système de fichiers local.
dst_doc.append_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING)
dst_doc.save(file_name=ARTIFACTS_DIR + 'Document.AppendDocument.docx')
```

Shows how to append all the documents in a folder to the end of a template document.

```python
dst_doc = aw.Document()
builder = aw.DocumentBuilder(doc=dst_doc)
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Template Document')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.NORMAL
builder.writeln('Some content here')
# Ajoutez tous les documents non chiffrés avec l'extension .doc
# depuis notre répertoire du système de fichiers local vers le document de base.
doc_files = list(filter(lambda item: item.endswith('.doc'), list(system_helper.io.Directory.get_files(MY_DIR, '*.doc'))))
for file_name in doc_files:
    info = aw.FileFormatUtil.detect_file_format(file_name=file_name)
    if info.is_encrypted:
        continue
    src_doc = aw.Document(file_name=file_name)
    dst_doc.append_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.USE_DESTINATION_STYLES)
dst_doc.save(file_name=ARTIFACTS_DIR + 'Document.AppendAllDocumentsInFolder.doc')
```

Shows how to manage list style clashes while appending a document.

```python
# Chargez un document contenant du texte dans un style personnalisé et clonez‑le.
src_doc = aw.Document(file_name=MY_DIR + 'Custom list numbering.docx')
dst_doc = src_doc.clone()
# Nous avons maintenant deux documents, chacun avec un style identique nommé "CustomStyle".
# Modifiez la couleur du texte pour l'un des styles afin de le distinguer de l'autre.
dst_doc.styles.get_by_name('CustomStyle').font.color = aspose.pydrawing.Color.dark_red
# S'il y a un conflit de styles de listes, appliquez le format de liste du document source.
# Définissez la propriété "KeepSourceNumbering" sur "false" pour ne pas importer de numéros de liste dans le document de destination.
# Définissez la propriété "KeepSourceNumbering" sur "true" pour importer tout ce qui entre en conflit
# Numérotation de style de liste avec la même apparence qu’elle avait dans le document source.
options = aw.ImportFormatOptions()
options.keep_source_numbering = keep_source_numbering
# Fusionner deux documents qui ont des styles différents portant le même nom provoque un conflit de style.
# Nous pouvons spécifier un mode de format d’importation lors de l’ajout de documents pour résoudre ce conflit.
dst_doc.append_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.KEEP_DIFFERENT_STYLES, import_format_options=options)
dst_doc.update_list_labels()
dst_doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.AppendDocumentAndResolveStyles.docx')
```

Shows how to manage list style clashes while inserting a document.

```python
dst_doc = aw.Document()
builder = aw.DocumentBuilder(doc=dst_doc)
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
dst_doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
doc_list = dst_doc.lists[0]
builder.list_format.list = doc_list
i = 1
while i <= 15:
    builder.write(f'List Item {i}\n')
    i += 1
attach_doc = dst_doc.clone(True).as_document()
# S'il y a un conflit de styles de listes, appliquez le format de liste du document source.
# Définissez la propriété "KeepSourceNumbering" sur "false" pour ne pas importer de numéros de liste dans le document de destination.
# Définissez la propriété "KeepSourceNumbering" sur "true" pour importer tout ce qui entre en conflit
# Numérotation de style de liste avec la même apparence qu’elle avait dans le document source.
import_options = aw.ImportFormatOptions()
import_options.keep_source_numbering = keep_source_numbering
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.insert_document(src_doc=attach_doc, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, import_format_options=import_options)
dst_doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertDocumentAndResolveStyles.docx')
```

Shows how to manage list style clashes while appending a clone of a document to itself.

```python
src_doc = aw.Document(file_name=MY_DIR + 'List item.docx')
dst_doc = aw.Document(file_name=MY_DIR + 'List item.docx')
# S'il y a un conflit de styles de listes, appliquez le format de liste du document source.
# Définissez la propriété "KeepSourceNumbering" sur "false" pour ne pas importer de numéros de liste dans le document de destination.
# Définissez la propriété "KeepSourceNumbering" sur "true" pour importer tout ce qui entre en conflit
# Numérotation de style de liste avec la même apparence qu’elle avait dans le document source.
builder = aw.DocumentBuilder(doc=dst_doc)
builder.move_to_document_end()
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
options = aw.ImportFormatOptions()
options.keep_source_numbering = keep_source_numbering
builder.insert_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, import_format_options=options)
dst_doc.update_list_labels()
```

## See Also

* module [aspose.words](../../)
* class [Document](../)


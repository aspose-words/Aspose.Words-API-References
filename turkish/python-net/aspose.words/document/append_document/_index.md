---
title: Document.append_document method
linktitle: append_document method
articleTitle: append_document method
second_title: Aspose.Words for Python
description: "aspose.words.Document.append_document method"
type: docs
weight: 580
url: /tr/python-net/aspose.words/document/append_document/
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
# Kaynak belgeyi, biçimlendirmesini koruyarak hedef belgeye ekleyin,
# daha sonra kaynak belgeyi yerel dosya sistemine kaydedin.
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
# .doc uzantılı tüm şifrelenmemiş belgeleri ekleyin
# yerel dosya sistemi dizinimizden temel belgeye.
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
# Özel bir stilde metin içeren bir belgeyi yükleyin ve klonlayın.
src_doc = aw.Document(file_name=MY_DIR + 'Custom list numbering.docx')
dst_doc = src_doc.clone()
# Şimdi, her biri "CustomStyle" adlı aynı stile sahip iki belgemiz var.
# Stillerden birinin metin rengini değiştirerek diğerinden ayırın.
dst_doc.styles.get_by_name('CustomStyle').font.color = aspose.pydrawing.Color.dark_red
# Liste stillerinde bir çakışma varsa, kaynak belgenin liste formatını uygulayın.
# "KeepSourceNumbering" özelliğini "false" olarak ayarlayarak, hedef belgeye herhangi bir liste numarası ithal etmeyin.
# "KeepSourceNumbering" özelliğini "true" olarak ayarlayın, tüm çakışanları içe aktar.
# Kaynak belgede olduğu gibi aynı görünüme sahip liste stili numaralandırması.
options = aw.ImportFormatOptions()
options.keep_source_numbering = keep_source_numbering
# Aynı adı paylaşan farklı stillere sahip iki belgeyi birleştirmek bir stil çakışmasına neden olur.
# Bu çakışmayı çözmek için belgeleri eklerken bir içe aktarma formatı modu belirtebiliriz.
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
# Liste stillerinde bir çakışma varsa, kaynak belgenin liste formatını uygulayın.
# "KeepSourceNumbering" özelliğini "false" olarak ayarlayarak, hedef belgeye herhangi bir liste numarası ithal etmeyin.
# "KeepSourceNumbering" özelliğini "true" olarak ayarlayın, tüm çakışanları içe aktar.
# Kaynak belgede olduğu gibi aynı görünüme sahip liste stili numaralandırması.
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
# Liste stillerinde bir çakışma varsa, kaynak belgenin liste formatını uygulayın.
# "KeepSourceNumbering" özelliğini "false" olarak ayarlayarak, hedef belgeye herhangi bir liste numarası ithal etmeyin.
# "KeepSourceNumbering" özelliğini "true" olarak ayarlayın, tüm çakışanları içe aktar.
# Kaynak belgede olduğu gibi aynı görünüme sahip liste stili numaralandırması.
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


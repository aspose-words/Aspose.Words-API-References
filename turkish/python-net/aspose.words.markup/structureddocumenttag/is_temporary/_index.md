---
title: StructuredDocumentTag.is_temporary property
linktitle: is_temporary property
articleTitle: is_temporary property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.is_temporary property. Specifies whether this SDT shall be removed from the WordProcessingML document when its contents are modified."
type: docs
weight: 160
url: /tr/python-net/aspose.words.markup/structureddocumenttag/is_temporary/
---

## StructuredDocumentTag.is_temporary property

Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents
are modified.



```python
@property
def is_temporary(self) -> bool:
    ...

@is_temporary.setter
def is_temporary(self, value: bool):
    ...

```

### Examples

Shows how to make single-use controls.

```python
doc = aw.Document()
# Düz metin bir yapılandırılmış belge etiketi ekleyin,
# bu, kullanıcının metin girebileceği düz metin bir form olarak hareket eder.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Yapılandırılmış belge etiketinin kaybolmasını sağlamak için "IsTemporary" özelliğini "true" olarak ayarlayın ve
# Kullanıcı Microsoft Word'de bir kez düzenledikten sonra içeriğini belgeye bütünleştirin.
# "IsTemporary" özelliğini "false" olarak ayarlayarak kullanıcının içeriği düzenlemesine izin verin
# yapılandırılmış belge etiketinin içeriğini istediğiniz sayıda kez düzenleyebilmesini.
tag.is_temporary = is_temporary
builder = aw.DocumentBuilder(doc=doc)
builder.write('Please enter text: ')
builder.insert_node(tag)
# Bir onay kutusu şeklinde başka bir yapılandırılmış belge etiketi ekleyin ve varsayılan durumunu "checked" olarak ayarlayın.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.CHECKBOX, aw.markup.MarkupLevel.INLINE)
tag.checked = True
# "IsTemporary" özelliğini "true" olarak ayarlayarak onay kutusunun bir simgeye dönüşmesini sağlayın
# kullanıcı Microsoft Word'de ona tıkladığında.
# "IsTemporary" özelliğini "false" olarak ayarlayarak kullanıcının onay kutusuna istediği kadar tıklamasına izin verin.
tag.is_temporary = is_temporary
builder.write('\nPlease click the check box: ')
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.IsTemporary.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)


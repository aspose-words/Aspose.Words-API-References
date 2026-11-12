---
title: Document.update_list_labels method
linktitle: update_list_labels method
articleTitle: update_list_labels method
second_title: Aspose.Words for Python
description: "Document.update_list_labels method. Updates list labels for all list items in the document."
type: docs
weight: 810
url: /tr/python-net/aspose.words/document/update_list_labels/
---

## update_list_labels() {#default}

Updates list labels for all list items in the document.


```python
def update_list_labels(self):
    ...
```

### Remarks

This method updates list label properties such as [ListLabel.label_value](../../../aspose.words.lists/listlabel/label_value/) and
[ListLabel.label_string](../../../aspose.words.lists/listlabel/label_string/) for each [Paragraph.list_label](../../paragraph/list_label/) object in the document.

Also, this method is sometimes implicitly called when updating fields in the document. This is required
because some fields that may reference list numbers (such as TOC or REF) need them be up-to-date.




### Examples

Shows how to extract the list labels of all paragraphs that are list items.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
doc.update_list_labels()
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
# Paragraf listesinin olup olmadığını bulun. Belgemizde, listemiz düz Arap rakamları kullanıyor,
# üçten başlayıp altıya kadar devam eder.
for paragraph in list(filter(lambda p: p.list_format.is_list_item, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_paragraph(), b), list(paras)))))):
    print(f'List item paragraph #{paras.index_of(paragraph)}')
    # Bu, bu düğümü metin formatına çıkardığımızda aldığımız metindir.
    # Bu metin çıktısı liste etiketlerini atlayacaktır. Herhangi bir paragraf biçimlendirme karakterini temizleyin.
    paragraph_text = paragraph.to_string(save_format=aw.SaveFormat.TEXT).strip()
    print(f'\tExported Text: {paragraph_text}')
    label = paragraph.list_label
    # Bu, paragrafın listedeki mevcut seviyedeki konumunu alır. Birden fazla seviyeye sahip bir listemiz varsa,
    # bu, o seviyedeki konumunu bize söyleyecektir.
    print(f'\tNumerical Id: {label.label_value}')
    # Çıktıda metinle birlikte liste etiketini eklemek için bunları birleştirin.
    print(f'\tList label combined with text: {label.label_string} {paragraph_text}')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)


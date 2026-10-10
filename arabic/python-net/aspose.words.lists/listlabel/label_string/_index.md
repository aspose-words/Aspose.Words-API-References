---
title: ListLabel.label_string property
linktitle: label_string property
articleTitle: label_string property
second_title: Aspose.Words for Python
description: "ListLabel.label_string property. Gets a string representation of list label."
type: docs
weight: 20
url: /ar/python-net/aspose.words.lists/listlabel/label_string/
---

## ListLabel.label_string property

Gets a string representation of list label.


```python
@property
def label_string(self) -> str:
    ...

```

### Examples

Shows how to extract the list labels of all paragraphs that are list items.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
doc.update_list_labels()
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
# ابحث عما إذا كان لدينا قائمة الفقرات. في مستندنا، تستخدم قائمتنا أرقام عربية عادية،
# التي تبدأ من ثلاثة وتنتهي عند ستة.
for paragraph in list(filter(lambda p: p.list_format.is_list_item, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_paragraph(), b), list(paras)))))):
    print(f'List item paragraph #{paras.index_of(paragraph)}')
    # هذا هو النص الذي نحصل عليه عند إخراج هذه العقدة إلى تنسيق نص.
    # سيتم حذف تسميات القائمة في إخراج النص هذا. قم بإزالة أي أحرف تنسيق الفقرة.
    paragraph_text = paragraph.to_string(save_format=aw.SaveFormat.TEXT).strip()
    print(f'\tExported Text: {paragraph_text}')
    label = paragraph.list_label
    # هذا يحصل على موضع الفقرة في المستوى الحالي للقائمة. إذا كان لدينا قائمة متعددة المستويات،
    # سيخبرنا هذا ما هو الموضع في ذلك المستوى.
    print(f'\tNumerical Id: {label.label_value}')
    # اجمعهما معًا لتضمين تسمية القائمة مع النص في الإخراج.
    print(f'\tList label combined with text: {label.label_string} {paragraph_text}')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLabel](../)


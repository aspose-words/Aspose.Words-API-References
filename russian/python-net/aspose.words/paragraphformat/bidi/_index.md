---
title: ParagraphFormat.bidi property
linktitle: bidi property
articleTitle: bidi property
second_title: Aspose.Words for Python
description: "ParagraphFormat.bidi property. Gets or sets whether this is a right-to-left paragraph."
type: docs
weight: 50
url: /ru/python-net/aspose.words/paragraphformat/bidi/
---

## ParagraphFormat.bidi property

Gets or sets whether this is a right-to-left paragraph.


```python
@property
def bidi(self) -> bool:
    ...

@bidi.setter
def bidi(self, value: bool):
    ...

```

### Remarks

When ``True``, the runs and other inline objects in this paragraph
are laid out right to left.




### Examples

Shows how to create right-to-left language-compatible lists with BIDIOUTLINE fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Поле BIDIOUTLINE нумерует абзацы так же, как поля AUTONUM/LISTNUM,
# но оно видно только при включённом языке редактирования справа налево, таком как иврит или арабский.
# Следующее поле отобразит ".1", RTL‑эквивалент номера списка "1.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True).as_field_bidi_outline()
builder.writeln('שלום')
self.assertEqual(' BIDIOUTLINE ', field.get_field_code())
# Добавьте ещё два поля BIDIOUTLINE, которые отобразят ".2" и ".3".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
# Установите горизонтальное выравнивание текста для каждого абзаца в документе в RTL.
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    para.paragraph_format.bidi = True
# Если мы включим язык редактирования справа налево в Microsoft Word, наши поля будут отображать числа.
# В противном случае они отобразят "###".
doc.save(file_name=ARTIFACTS_DIR + 'Field.BIDIOUTLINE.docx')
```

Shows how to detect plaintext document text direction.

```python
# Создайте объект "TxtLoadOptions", который мы можем передать конструктору документа
# чтобы изменить способ загрузки обычного текстового документа.
load_options = aw.loading.TxtLoadOptions()
# Установите свойство "DocumentDirection" в значение "DocumentDirection.Auto", которое автоматически определяет
# направление каждого абзаца текста, который Aspose.Words загружает из обычного текста.
# Свойство "Bidi" каждого абзаца будет хранить его направление.
load_options.document_direction = aw.loading.DocumentDirection.AUTO
# Обнаруживать иврит как текст справа налево.
doc = aw.Document(file_name=MY_DIR + 'Hebrew text.txt', load_options=load_options)
self.assertTrue(doc.first_section.body.first_paragraph.paragraph_format.bidi)
# Обнаруживать английский текст как справа налево.
doc = aw.Document(file_name=MY_DIR + 'English text.txt', load_options=load_options)
self.assertFalse(doc.first_section.body.first_paragraph.paragraph_format.bidi)
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)


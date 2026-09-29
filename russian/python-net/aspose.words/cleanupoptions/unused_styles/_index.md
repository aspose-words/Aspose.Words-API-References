---
title: CleanupOptions.unused_styles property
linktitle: unused_styles property
articleTitle: unused_styles property
second_title: Aspose.Words for Python
description: "CleanupOptions.unused_styles property. Specifies whether unused styles should be removed from document"
type: docs
weight: 50
url: /ru/python-net/aspose.words/cleanupoptions/unused_styles/
---

## CleanupOptions.unused_styles property

Specifies whether unused styles should be removed from document.
Default value is ``True``.



```python
@property
def unused_styles(self) -> bool:
    ...

@unused_styles.setter
def unused_styles(self, value: bool):
    ...

```

### Examples

Shows how to remove all unused custom styles from a document.

```python
doc = aw.Document()
doc.styles.add(aw.StyleType.LIST, 'MyListStyle1')
doc.styles.add(aw.StyleType.LIST, 'MyListStyle2')
doc.styles.add(aw.StyleType.CHARACTER, 'MyParagraphStyle1')
doc.styles.add(aw.StyleType.CHARACTER, 'MyParagraphStyle2')
# В сочетании со встроенными стилями документ теперь имеет восемь стилей.
# Пользовательский стиль помечается как «использованный», пока в документе присутствует любой текст.
# отформатированный в этом стиле. Это означает, что 4 добавленных нами стиля в данный момент не используются.
self.assertEqual(8, doc.styles.count)
# Примените пользовательский символьный стиль, а затем пользовательский список‑стиль. Это пометит их как «использованные».
builder = aw.DocumentBuilder(doc=doc)
builder.font.style = doc.styles.get_by_name('MyParagraphStyle1')
builder.writeln('Hello world!')
doc_list = doc.lists.add(list_style=doc.styles.get_by_name('MyListStyle1'))
builder.list_format.list = doc_list
builder.writeln('Item 1')
builder.writeln('Item 2')
# Сейчас есть один неиспользуемый символьный стиль и один неиспользуемый список‑стиль.
# Метод Cleanup() при настройке с объектом CleanupOptions может находить неиспользуемые стили и удалять их.
cleanup_options = aw.CleanupOptions()
cleanup_options.unused_lists = True
cleanup_options.unused_styles = True
cleanup_options.unused_builtin_styles = True
doc.cleanup(cleanup_options)
self.assertEqual(4, doc.styles.count)
# Удаление каждого узла, к которому применён пользовательский стиль, снова помечает его как «неиспользуемый».
# Повторно запустите метод Cleanup, чтобы удалить их.
doc.first_section.body.remove_all_children()
doc.cleanup(cleanup_options)
self.assertEqual(2, doc.styles.count)
```

### See Also

* module [aspose.words](../../)
* class [CleanupOptions](../)


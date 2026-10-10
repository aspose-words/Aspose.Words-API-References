---
title: CleanupOptions.unused_builtin_styles property
linktitle: unused_builtin_styles property
articleTitle: unused_builtin_styles property
second_title: Aspose.Words for Python
description: "CleanupOptions.unused_builtin_styles property. Specifies that unused [Style.built_in](../../style/built_in/) styles should be removed from document."
type: docs
weight: 30
url: /sv/python-net/aspose.words/cleanupoptions/unused_builtin_styles/
---

## CleanupOptions.unused_builtin_styles property

Specifies that unused [Style.built_in](../../style/built_in/) styles should be removed from document.



```python
@property
def unused_builtin_styles(self) -> bool:
    ...

@unused_builtin_styles.setter
def unused_builtin_styles(self, value: bool):
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
# Kombinerat med de inbyggda stilarna har dokumentet nu åtta stilar.
# En anpassad stil markeras som "använd" så länge det finns någon text i dokumentet
# formaterad i den stilen. Detta betyder att de 4 stilar vi lade till för närvarande är oanvända.
self.assertEqual(8, doc.styles.count)
# Applicera en anpassad teckenstil och sedan en anpassad liststil. Att göra så markerar dem som "använd".
builder = aw.DocumentBuilder(doc=doc)
builder.font.style = doc.styles.get_by_name('MyParagraphStyle1')
builder.writeln('Hello world!')
doc_list = doc.lists.add(list_style=doc.styles.get_by_name('MyListStyle1'))
builder.list_format.list = doc_list
builder.writeln('Item 1')
builder.writeln('Item 2')
# Nu finns det en oanvänd teckenstil och en oanvänd liststil.
# Metoden Cleanup() kan, när den konfigureras med ett CleanupOptions-objekt, rikta in sig på oanvända stilar och ta bort dem.
cleanup_options = aw.CleanupOptions()
cleanup_options.unused_lists = True
cleanup_options.unused_styles = True
cleanup_options.unused_builtin_styles = True
doc.cleanup(cleanup_options)
self.assertEqual(4, doc.styles.count)
# Att ta bort varje nod som en anpassad stil tillämpas på markerar den som "oanvänd" igen.
# Kör Cleanup-metoden igen för att ta bort dem.
doc.first_section.body.remove_all_children()
doc.cleanup(cleanup_options)
self.assertEqual(2, doc.styles.count)
```

### See Also

* module [aspose.words](../../)
* class [CleanupOptions](../)


---
title: CleanupOptions.unused_styles property
linktitle: unused_styles property
articleTitle: unused_styles property
second_title: Aspose.Words for Python
description: "CleanupOptions.unused_styles property. Specifies whether unused styles should be removed from document"
type: docs
weight: 50
url: /fr/python-net/aspose.words/cleanupoptions/unused_styles/
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
# Combiné aux styles intégrés, le document possède maintenant huit styles.
# Un style personnalisé est marqué comme "utilisé" tant qu'il y a du texte dans le document
# formaté avec ce style. Cela signifie que les 4 styles que nous avons ajoutés sont actuellement inutilisés.
self.assertEqual(8, doc.styles.count)
# Appliquez un style de caractère personnalisé, puis un style de liste personnalisé. Cela les marquera comme "utilisés".
builder = aw.DocumentBuilder(doc=doc)
builder.font.style = doc.styles.get_by_name('MyParagraphStyle1')
builder.writeln('Hello world!')
doc_list = doc.lists.add(list_style=doc.styles.get_by_name('MyListStyle1'))
builder.list_format.list = doc_list
builder.writeln('Item 1')
builder.writeln('Item 2')
# À présent, il y a un style de caractère inutilisé et un style de liste inutilisé.
# La méthode Cleanup(), lorsqu'elle est configurée avec un objet CleanupOptions, peut cibler les styles inutilisés et les supprimer.
cleanup_options = aw.CleanupOptions()
cleanup_options.unused_lists = True
cleanup_options.unused_styles = True
cleanup_options.unused_builtin_styles = True
doc.cleanup(cleanup_options)
self.assertEqual(4, doc.styles.count)
# Supprimer chaque nœud auquel un style personnalisé est appliqué le marque à nouveau comme "inutilisé".
# Réexécutez la méthode Cleanup pour les supprimer.
doc.first_section.body.remove_all_children()
doc.cleanup(cleanup_options)
self.assertEqual(2, doc.styles.count)
```

### See Also

* module [aspose.words](../../)
* class [CleanupOptions](../)


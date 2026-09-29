---
title: CleanupOptions class
linktitle: CleanupOptions class
articleTitle: CleanupOptions class
second_title: Aspose.Words for Python
description: "aspose.words.CleanupOptions class. Allows to specify options for document cleaning"
type: docs
weight: 160
url: /tr/python-net/aspose.words/cleanupoptions/
---

## CleanupOptions class

Allows to specify options for document cleaning.
To learn more, visit the [Clean Up a Document](https://docs.aspose.com/words/python-net/clean-up-a-document/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [CleanupOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [duplicate_style](./duplicate_style/) | Gets/sets a flag indicating whether duplicate styles should be removed from document. Default value is ``False``. |
| [unused_builtin_styles](./unused_builtin_styles/) | Specifies that unused [Style.built_in](../style/built_in/) styles should be removed from document. |
| [unused_lists](./unused_lists/) | Specifies whether unused list and list definitions should be removed from document. Default value is ``True``. |
| [unused_styles](./unused_styles/) | Specifies whether unused styles should be removed from document. Default value is ``True``. |

### Examples

Shows how to remove all unused custom styles from a document.

```python
doc = aw.Document()
doc.styles.add(aw.StyleType.LIST, 'MyListStyle1')
doc.styles.add(aw.StyleType.LIST, 'MyListStyle2')
doc.styles.add(aw.StyleType.CHARACTER, 'MyParagraphStyle1')
doc.styles.add(aw.StyleType.CHARACTER, 'MyParagraphStyle2')
# Yerleşik stillerle birleştirildiğinde, belgenin artık sekiz stili var.
# Belge içinde herhangi bir metin olduğu sürece özel bir stil "kullanılıyor" olarak işaretlenir
# bu stil ile biçimlendirilir. Bu, eklediğimiz 4 stilin şu anda kullanılmadığı anlamına gelir.
self.assertEqual(8, doc.styles.count)
# Özel bir karakter stili uygulayın, ardından özel bir liste stili uygulayın. Bunu yapmak onları "kullanılıyor" olarak işaretleyecek.
builder = aw.DocumentBuilder(doc=doc)
builder.font.style = doc.styles.get_by_name('MyParagraphStyle1')
builder.writeln('Hello world!')
doc_list = doc.lists.add(list_style=doc.styles.get_by_name('MyListStyle1'))
builder.list_format.list = doc_list
builder.writeln('Item 1')
builder.writeln('Item 2')
# Şimdi, bir kullanılmayan karakter stili ve bir kullanılmayan liste stili var.
# Cleanup() yöntemi, bir CleanupOptions nesnesiyle yapılandırıldığında, kullanılmayan stilleri hedef alabilir ve kaldırabilir.
cleanup_options = aw.CleanupOptions()
cleanup_options.unused_lists = True
cleanup_options.unused_styles = True
cleanup_options.unused_builtin_styles = True
doc.cleanup(cleanup_options)
self.assertEqual(4, doc.styles.count)
# Özel bir stilin uygulandığı her düğümü kaldırmak, stili tekrar "kullanılmıyor" olarak işaretler.
# Onları kaldırmak için Cleanup yöntemini yeniden çalıştırın.
doc.first_section.body.remove_all_children()
doc.cleanup(cleanup_options)
self.assertEqual(2, doc.styles.count)
```

### See Also

* module [aspose.words](../)


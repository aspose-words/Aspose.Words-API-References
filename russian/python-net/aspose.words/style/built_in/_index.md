---
title: Style.built_in property
linktitle: built_in property
articleTitle: built_in property
second_title: Aspose.Words for Python
description: "Style.built_in property. True if this style is one of the built-in styles in MS Word."
type: docs
weight: 40
url: /ru/python-net/aspose.words/style/built_in/
---

## Style.built_in property

True if this style is one of the built-in styles in MS Word.


```python
@property
def built_in(self) -> bool:
    ...

```

### Examples

Shows how to differentiate custom styles from built-in styles.

```python
doc = aw.Document()
# Когда мы создаём документ с помощью Microsoft Word или программно, используя Aspose.Words,
# документ будет содержать коллекцию стилей, которые можно применить к его тексту для изменения внешнего вида.
# Мы можем получить доступ к этим встроенным стилям через коллекцию "Styles" документа.
# У всех этих стилей будет установлен флаг "BuiltIn" со значением "true".
style = doc.styles.get_by_name('Emphasis')
self.assertTrue(style.built_in)
# Создайте пользовательский стиль и добавьте его в коллекцию.
# У пользовательских стилей, подобных этому, флаг "BuiltIn" будет установлен в "false".
style = doc.styles.add(aw.StyleType.CHARACTER, 'MyStyle')
style.font.color = aspose.pydrawing.Color.navy
style.font.name = 'Courier New'
self.assertFalse(style.built_in)
```

### See Also

* module [aspose.words](../../)
* class [Style](../)


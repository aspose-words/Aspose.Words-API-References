---
title: Style.built_in property
linktitle: built_in property
articleTitle: built_in property
second_title: Aspose.Words for Python
description: "Style.built_in property. True if this style is one of the built-in styles in MS Word."
type: docs
weight: 40
url: /es/python-net/aspose.words/style/built_in/
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
# Cuando creamos un documento usando Microsoft Word, o programáticamente usando Aspose.Words,
# el documento vendrá con una colección de estilos para aplicar a su texto y modificar su apariencia.
# Podemos acceder a estos estilos incorporados a través de la colección "Styles" del documento.
# Todos estos estilos tendrán la bandera "BuiltIn" establecida en "true".
style = doc.styles.get_by_name('Emphasis')
self.assertTrue(style.built_in)
# Cree un estilo personalizado y agréguelo a la colección.
# Los estilos personalizados como este tendrán la bandera "BuiltIn" establecida en "false".
style = doc.styles.add(aw.StyleType.CHARACTER, 'MyStyle')
style.font.color = aspose.pydrawing.Color.navy
style.font.name = 'Courier New'
self.assertFalse(style.built_in)
```

### See Also

* module [aspose.words](../../)
* class [Style](../)


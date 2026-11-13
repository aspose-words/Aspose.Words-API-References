---
title: CustomXmlPropertyCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "CustomXmlPropertyCollection.add method. Adds a property to the collection."
type: docs
weight: 30
url: /es/python-net/aspose.words.markup/customxmlpropertycollection/add/
---

## add(property) {#customxmlproperty}

Adds a property to the collection.


```python
def add(self, property: aspose.words.markup.CustomXmlProperty):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| property | [CustomXmlProperty](../../customxmlproperty/) | The property to add. |

### Examples

Shows how to work with smart tag properties to get in depth information about smart tags.

```python
doc = aw.Document(file_name=MY_DIR + 'Smart tags.doc')
# Una etiqueta inteligente aparece en un documento con Microsoft Word que reconoce una parte de su texto como algún tipo de dato,
# como un nombre, una fecha o una dirección, y la convierte en un hipervínculo que muestra un subrayado punteado púrpura.
# En Word 2003, podemos habilitar las etiquetas inteligentes mediante "Tools" -> "AutoCorrect options..." -> "SmartTags".
# En nuestro documento de entrada, hay tres objetos que Microsoft Word registró como etiquetas inteligentes.
# Las etiquetas inteligentes pueden estar anidadas, por lo que esta colección contiene más.
smart_tags = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_smart_tag(), b), list(doc.get_child_nodes(aw.NodeType.SMART_TAG, True)))))
self.assertEqual(8, len(smart_tags))
# El miembro "Properties" de una etiqueta inteligente contiene sus metadatos, que serán diferentes para cada tipo de etiqueta inteligente.
# Las propiedades de una etiqueta inteligente de tipo "date" contienen su año, mes y día.
properties = smart_tags[7].properties
self.assertEqual(4, properties.count)
for current in properties:
    print(f'Property name: {current.name}, value: {current.value}')
    self.assertEqual('', current.uri)
# También podemos acceder a las propiedades de varias maneras, como un par clave-valor.
self.assertTrue(properties.contains('Day'))
self.assertEqual('22', properties.get_by_name('Day').value)
self.assertEqual('2003', properties[2].value)
self.assertEqual(1, properties.index_of_key('Month'))
# A continuación se presentan tres formas de eliminar elementos de la colección de propiedades.
# 1 -  Eliminar por índice:
properties.remove_at(3)
self.assertEqual(3, properties.count)
# 2 -  Eliminar por nombre:
properties.remove('Year')
self.assertEqual(2, properties.count)
# 3 -  Borrar toda la colección de una vez:
properties.clear()
self.assertEqual(0, properties.count)
```

### See Also

* module [aspose.words.markup](../../)
* class [CustomXmlPropertyCollection](../)


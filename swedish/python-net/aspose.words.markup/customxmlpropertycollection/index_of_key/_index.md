---
title: CustomXmlPropertyCollection.index_of_key method
linktitle: index_of_key method
articleTitle: index_of_key method
second_title: Aspose.Words for Python
description: "CustomXmlPropertyCollection.index_of_key method. Returns the zero-based index of the specified property in the collection."
type: docs
weight: 70
url: /sv/python-net/aspose.words.markup/customxmlpropertycollection/index_of_key/
---

## index_of_key(name) {#str}

Returns the zero-based index of the specified property in the collection.


```python
def index_of_key(self, name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | The case-sensitive name of the property. |

### Returns

The zero based index. Negative value if not found.


### Examples

Shows how to work with smart tag properties to get in depth information about smart tags.

```python
doc = aw.Document(file_name=MY_DIR + 'Smart tags.doc')
# En smarttagg visas i ett dokument där Microsoft Word känner igen en del av dess text som någon form av data,
# såsom ett namn, datum eller adress, och konverterar den till en hyperlänk som visar en lila prickad understrykning.
# I Word 2003 kan vi aktivera smarta taggar via "Tools" -> "AutoCorrect options..." -> "SmartTags".
# I vårt inmatningsdokument finns tre objekt som Microsoft Word registrerade som smarta taggar.
# Smarta taggar kan vara nästlade, så den här samlingen innehåller fler.
smart_tags = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_smart_tag(), b), list(doc.get_child_nodes(aw.NodeType.SMART_TAG, True)))))
self.assertEqual(8, len(smart_tags))
# Medlemmen "Properties" i en smart tagg innehåller dess metadata, som kommer att vara olika för varje typ av smart tagg.
# Egenskaperna för en smart tagg av typen "date" innehåller dess år, månad och dag.
properties = smart_tags[7].properties
self.assertEqual(4, properties.count)
for current in properties:
    print(f'Property name: {current.name}, value: {current.value}')
    self.assertEqual('', current.uri)
# Vi kan också komma åt egenskaperna på olika sätt, till exempel som ett nyckel‑värde‑par.
self.assertTrue(properties.contains('Day'))
self.assertEqual('22', properties.get_by_name('Day').value)
self.assertEqual('2003', properties[2].value)
self.assertEqual(1, properties.index_of_key('Month'))
# Nedan följer tre sätt att ta bort element från egenskapskollektionen.
# 1 -  Ta bort efter index:
properties.remove_at(3)
self.assertEqual(3, properties.count)
# 2 -  Ta bort efter namn:
properties.remove('Year')
self.assertEqual(2, properties.count)
# 3 -  Rensa hela samlingen på en gång:
properties.clear()
self.assertEqual(0, properties.count)
```

### See Also

* module [aspose.words.markup](../../)
* class [CustomXmlPropertyCollection](../)


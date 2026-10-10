---
title: CustomXmlPropertyCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "CustomXmlPropertyCollection.clear method. Removes all elements from the collection."
type: docs
weight: 40
url: /de/python-net/aspose.words.markup/customxmlpropertycollection/clear/
---

## clear() {#default}

Removes all elements from the collection.


```python
def clear(self):
    ...
```

### Examples

Shows how to work with smart tag properties to get in depth information about smart tags.

```python
doc = aw.Document(file_name=MY_DIR + 'Smart tags.doc')
# Ein Smart‑Tag erscheint in einem Dokument, wenn Microsoft Word einen Teil seines Textes als eine Art von Daten erkennt,
# wie einen Namen, ein Datum oder eine Adresse, und wandelt ihn in einen Hyperlink um, der einen lila gepunkteten Unterstrich anzeigt.
# In Word 2003 können wir SmartTags über "Tools" -> "AutoCorrect options..." -> "SmartTags" aktivieren.
# In unserem Eingabedokument gibt es drei Objekte, die Microsoft Word als SmartTags registriert hat.
# SmartTags können verschachtelt sein, daher enthält diese Sammlung mehr.
smart_tags = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_smart_tag(), b), list(doc.get_child_nodes(aw.NodeType.SMART_TAG, True)))))
self.assertEqual(8, len(smart_tags))
# Das "Properties"-Element eines SmartTags enthält seine Metadaten, die für jeden Typ von SmartTag unterschiedlich sein werden.
# Die Eigenschaften eines "date"-Typ‑SmartTags enthalten sein Jahr, Monat und Tag.
properties = smart_tags[7].properties
self.assertEqual(4, properties.count)
for current in properties:
    print(f'Property name: {current.name}, value: {current.value}')
    self.assertEqual('', current.uri)
# Wir können auch auf die Eigenschaften auf verschiedene Arten zugreifen, zum Beispiel als Schlüssel‑Wert‑Paar.
self.assertTrue(properties.contains('Day'))
self.assertEqual('22', properties.get_by_name('Day').value)
self.assertEqual('2003', properties[2].value)
self.assertEqual(1, properties.index_of_key('Month'))
# Unten sind drei Methoden zum Entfernen von Elementen aus der Eigenschaften‑Sammlung aufgeführt.
# 1 -  Entfernen nach Index:
properties.remove_at(3)
self.assertEqual(3, properties.count)
# 2 -  Entfernen nach Name:
properties.remove('Year')
self.assertEqual(2, properties.count)
# 3 -  Lösche die gesamte Sammlung auf einmal:
properties.clear()
self.assertEqual(0, properties.count)
```

### See Also

* module [aspose.words.markup](../../)
* class [CustomXmlPropertyCollection](../)


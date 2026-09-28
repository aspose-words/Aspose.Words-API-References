---
title: CustomXmlProperty.uri property
linktitle: uri property
articleTitle: uri property
second_title: Aspose.Words for Python
description: "CustomXmlProperty.uri property. Gets or sets the namespace URI of the custom XML attribute or smart tag property."
type: docs
weight: 30
url: /fr/python-net/aspose.words.markup/customxmlproperty/uri/
---

## CustomXmlProperty.uri property

Gets or sets the namespace URI of the custom XML attribute or smart tag property.


```python
@property
def uri(self) -> str:
    ...

@uri.setter
def uri(self, value: str):
    ...

```

### Remarks

Cannot be ``None``.

Default is empty string.




### Examples

Shows how to work with smart tag properties to get in depth information about smart tags.

```python
doc = aw.Document(file_name=MY_DIR + 'Smart tags.doc')
# Une balise intelligente apparaît dans un document avec Microsoft Word qui reconnaît une partie de son texte comme une forme de données,
# telle qu'un nom, une date ou une adresse, et la convertit en hyperlien affichant un soulignement pointillé violet.
# Dans Word 2003, nous pouvons activer les balises intelligentes via "Outils" -> "Options de correction automatique..." -> "SmartTags".
# Dans notre document d'entrée, il y a trois objets que Microsoft Word a enregistrés comme balises intelligentes.
# Les balises intelligentes peuvent être imbriquées, donc cette collection en contient davantage.
smart_tags = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_smart_tag(), b), list(doc.get_child_nodes(aw.NodeType.SMART_TAG, True)))))
self.assertEqual(8, len(smart_tags))
# Le membre "Properties" d'une balise intelligente contient ses métadonnées, qui seront différentes pour chaque type de balise intelligente.
# Les propriétés d'une balise intelligente de type "date" contiennent son année, son mois et son jour.
properties = smart_tags[7].properties
self.assertEqual(4, properties.count)
for current in properties:
    print(f'Property name: {current.name}, value: {current.value}')
    self.assertEqual('', current.uri)
# Nous pouvons également accéder aux propriétés de différentes manières, comme une paire clé-valeur.
self.assertTrue(properties.contains('Day'))
self.assertEqual('22', properties.get_by_name('Day').value)
self.assertEqual('2003', properties[2].value)
self.assertEqual(1, properties.index_of_key('Month'))
# Ci-dessous trois façons de supprimer des éléments de la collection de propriétés.
# 1 -  Supprimer par indice :
properties.remove_at(3)
self.assertEqual(3, properties.count)
# 2 -  Supprimer par nom :
properties.remove('Year')
self.assertEqual(2, properties.count)
# 3 -  Effacer toute la collection d'un coup :
properties.clear()
self.assertEqual(0, properties.count)
```

### See Also

* module [aspose.words.markup](../../)
* class [CustomXmlProperty](../)


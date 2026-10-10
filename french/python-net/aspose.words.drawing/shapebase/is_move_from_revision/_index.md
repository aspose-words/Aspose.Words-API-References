---
title: ShapeBase.is_move_from_revision property
linktitle: is_move_from_revision property
articleTitle: is_move_from_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_move_from_revision property. Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 340
url: /fr/python-net/aspose.words.drawing/shapebase/is_move_from_revision/
---

## ShapeBase.is_move_from_revision property

Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.



```python
@property
def is_move_from_revision(self) -> bool:
    ...

```

### Examples

Shows how to identify move revision shapes.

```python
# Une révision de déplacement se produit lorsque nous déplaçons un élément du corps du document en le couper‑coller dans Microsoft Word tout en
# suivant les modifications. Si nous impliquons une forme en ligne dans un tel déplacement de texte, cette forme sera également une révision.
# Copier‑coller ou déplacer des formes flottantes ne crée pas de révisions de déplacement.
doc = aw.Document(file_name=MY_DIR + 'Revision shape.docx')
# Les révisions de déplacement se composent de paires de révisions "Move from" et "Move to". Nous avons déplacé dans ce document une forme,
# mais tant que nous n'acceptons pas ou ne rejetons pas la révision de déplacement, il y aura deux instances de cette forme.
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
# Ceci est la révision "Move to", qui est la forme à son lieu d'arrivée.
# Si nous acceptons la révision, cette forme de révision "Move to" disparaîtra,
# et la forme de révision "Move from" restera.
self.assertFalse(shapes[0].is_move_from_revision)
self.assertTrue(shapes[0].is_move_to_revision)
# Ceci est la révision "Move from", qui est la forme à son emplacement d'origine.
# Si nous acceptons la révision, cette forme de révision "Move from" disparaîtra,
# et la forme de révision "Move to" restera.
self.assertTrue(shapes[1].is_move_from_revision)
self.assertFalse(shapes[1].is_move_to_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)


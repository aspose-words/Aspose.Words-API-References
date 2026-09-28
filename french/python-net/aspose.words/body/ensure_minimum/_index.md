---
title: Body.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Body.ensure_minimum method. If the last child is not a paragraph, creates and appends one empty paragraph."
type: docs
weight: 70
url: /fr/python-net/aspose.words/body/ensure_minimum/
---

## ensure_minimum() {#default}

If the last child is not a paragraph, creates and appends one empty paragraph.


```python
def ensure_minimum(self):
    ...
```

### Examples

Clears main text from all sections from the document leaving the sections themselves.

```python
doc = aw.Document()
# Un document vierge contient une section, un corps et un paragraphe.
# Appelez la méthode "RemoveAllChildren" pour supprimer tous ces nœuds,
# et vous vous retrouvez avec un nœud de document sans enfants.
doc.remove_all_children()
# Ce document n'a maintenant aucun nœud enfant composite auquel nous pouvons ajouter du contenu.
# Si nous souhaitons le modifier, nous devrons reconstituer sa collection de nœuds.
# Tout d'abord, créez une nouvelle section, puis ajoutez‑la en tant qu'enfant au nœud racine du document.
section = aw.Section(doc)
doc.append_child(section)
# Une section nécessite un corps, qui contiendra et affichera tout son contenu
# sur la page entre l'en‑tête et le pied‑de‑page de la section.
body = aw.Body(doc)
section.append_child(body)
# Ce corps n'a aucun enfant, nous ne pouvons donc pas encore y ajouter de runs.
self.assertEqual(0, doc.first_section.body.get_child_nodes(aw.NodeType.ANY, True).count)
# Appelez "EnsureMinimum" pour vous assurer que ce corps contient au moins un paragraphe vide.
body.ensure_minimum()
# Maintenant, nous pouvons ajouter des runs au corps, et faire afficher le document.
body.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Body](../)


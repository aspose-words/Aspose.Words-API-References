---
title: HeaderFooterCollection indexer
linktitle: HeaderFooterCollection indexer
articleTitle: HeaderFooterCollection indexer
second_title: Aspose.Words for Python
description: "HeaderFooterCollection indexer. Retrieves a [HeaderFooter](../../headerfooter/) at the given index."
type: docs
weight: 10
url: /fr/python-net/aspose.words/headerfootercollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Retrieves a [HeaderFooter](../../headerfooter/) at the given index.



```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. 
For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.




### Examples

Shows how to link headers and footers between sections.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Section 2')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Section 3')
# Déplacez‑vous vers la première section et créez un en‑tête et un pied de page. Par défaut,
# l’en‑tête et le pied de page n’apparaîtront que sur les pages de la section qui les contient.
builder.move_to_section(0)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('This is the header, which will be displayed in sections 1 and 2.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.write('This is the footer, which will be displayed in sections 1, 2 and 3.')
# Nous pouvons lier les en‑têtes/pieds de page d’une section à ceux de la section précédente
# pour permettre à la section de liaison d’afficher les en‑têtes/pieds de page de la section liée.
doc.sections[1].headers_footers.link_to_previous(is_link_to_previous=True)
# Chaque section aura toujours ses propres objets d’en‑tête/pied de page. Lorsque nous lions les sections,
# la section de liaison affichera les en‑têtes/pieds de page de la section liée tout en conservant les siens.
assert doc.sections[0].headers_footers[0] is not doc.sections[1].headers_footers[0]
assert doc.sections[0].headers_footers[0].parent_section is not doc.sections[1].headers_footers[0].parent_section
# Liez les en‑têtes/pieds de page de la troisième section à ceux de la deuxième section.
# La deuxième section est déjà liée aux en‑têtes/pieds de page de la première section,
# ainsi, lier à la deuxième section créera une chaîne de liens.
# Les première, deuxième et maintenant troisième sections afficheront toutes les en‑têtes de la première section.
doc.sections[2].headers_footers.link_to_previous(is_link_to_previous=True)
# Nous pouvons dés‑lier les en‑têtes/pieds de page d’une section précédente en passant "false" lors de l’appel de la méthode LinkToPrevious.
doc.sections[2].headers_footers.link_to_previous(is_link_to_previous=False)
# Nous pouvons également sélectionner uniquement un type spécifique d’en‑tête/pied de page à lier en utilisant cette méthode.
# La troisième section aura désormais le même pied de page que les deuxième et première sections, mais pas le même en‑tête.
doc.sections[2].headers_footers.link_to_previous(header_footer_type=aw.HeaderFooterType.FOOTER_PRIMARY, is_link_to_previous=True)
# Les en-têtes/pieds de page de la première section ne peuvent pas se lier à quoi que ce soit car il n'y a pas de section précédente.
self.assertEqual(2, doc.sections[0].headers_footers.count)
self.assertEqual(2, len(list(filter(lambda hf: not hf.as_header_footer().is_linked_to_previous, doc.sections[0].headers_footers))))
# Tous les en-têtes/pieds de page de la deuxième section sont liés aux en-têtes/pieds de page de la première section.
self.assertEqual(6, doc.sections[1].headers_footers.count)
self.assertEqual(6, len(list(filter(lambda hf: hf.as_header_footer().is_linked_to_previous, doc.sections[1].headers_footers))))
# Dans la troisième section, seul le pied de page est lié au pied de page de la première section via la deuxième section.
self.assertEqual(6, doc.sections[2].headers_footers.count)
self.assertEqual(5, len(list(filter(lambda hf: not hf.as_header_footer().is_linked_to_previous, doc.sections[2].headers_footers))))
self.assertTrue(doc.sections[2].headers_footers[3].is_linked_to_previous)
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.Link.docx')
```

### See Also

* module [aspose.words](../../)
* class [HeaderFooterCollection](../)


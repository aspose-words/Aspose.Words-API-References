---
title: ParagraphAlignment enumeration
linktitle: ParagraphAlignment enumeration
articleTitle: ParagraphAlignment enumeration
second_title: Aspose.Words for Python
description: "aspose.words.ParagraphAlignment enumeration. Specifies text alignment in a paragraph."
type: docs
weight: 970
url: /fr/python-net/aspose.words/paragraphalignment/
---

## ParagraphAlignment enumeration

Specifies text alignment in a paragraph.


### Members

| Name | Description |
| --- | --- |
| LEFT | Text is aligned to the left. |
| CENTER | Text is centered horizontally. |
| RIGHT | Text is aligned to the right. |
| JUSTIFY | Text is aligned to both left and right. |
| DISTRIBUTED | Text is evenly distributed. |
| ARABIC_MEDIUM_KASHIDA | Arabic only. Kashida length for text is extended to a medium length determined by the consumer. |
| ARABIC_HIGH_KASHIDA | Arabic only. Kashida length for text is extended to its widest possible length. |
| ARABIC_LOW_KASHIDA | Arabic only. Kashida length for text is extended to a slightly longer length. |
| THAI_DISTRIBUTED | Thai only. Text is justified with an optimization for Thai. |
| MATH_ELEMENT_CENTER_AS_GROUP | The only Math element in a line, aligned as 'Centered As Group'. |

### Examples

Shows how to construct an Aspose.Words document by hand.

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
# Définissez quelques propriétés de mise en page pour la section.
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER
# Une section nécessite un corps, qui contiendra et affichera tout son contenu
# sur la page entre l'en‑tête et le pied‑de‑page de la section.
body = aw.Body(doc)
section.append_child(body)
# Créez un paragraphe, définissez quelques propriétés de formatage, puis ajoutez‑le en tant qu'enfant au corps.
para = aw.Paragraph(doc)
para.paragraph_format.style_name = 'Heading 1'
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
body.append_child(para)
# Enfin, ajoutez du contenu au document. Créez un run,
# définissez son apparence et son contenu, puis ajoutez‑le en tant qu'enfant au paragraphe.
run = aw.Run(doc=doc)
run.text = 'Hello World!'
run.font.color = aspose.pydrawing.Color.red
para.append_child(run)
self.assertEqual('Hello World!', doc.get_text().strip())
doc.save(file_name=ARTIFACTS_DIR + 'Section.CreateManually.docx')
```

### See Also

* module [aspose.words](../)


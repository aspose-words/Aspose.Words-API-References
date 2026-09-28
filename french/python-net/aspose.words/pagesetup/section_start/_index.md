---
title: PageSetup.section_start property
linktitle: section_start property
articleTitle: section_start property
second_title: Aspose.Words for Python
description: "PageSetup.section_start property. Returns or sets the type of section break for the specified object."
type: docs
weight: 390
url: /fr/python-net/aspose.words/pagesetup/section_start/
---

## PageSetup.section_start property

Returns or sets the type of section break for the specified object.


```python
@property
def section_start(self) -> aspose.words.SectionStart:
    ...

@section_start.setter
def section_start(self, value: aspose.words.SectionStart):
    ...

```

### Examples

Shows how to specify how a new section separates itself from the previous.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('This text is in section 1.')
# Les types de saut de section déterminent comment une nouvelle section se sépare de la section précédente.
# Ci-dessous, cinq types de sauts de section.
# 1 -  Commence la section suivante sur une nouvelle page:
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln('This text is in section 2.')
self.assertEqual(aw.SectionStart.NEW_PAGE, doc.sections[1].page_setup.section_start)
# 2 -  Commence la section suivante sur la page actuelle:
builder.insert_break(aw.BreakType.SECTION_BREAK_CONTINUOUS)
builder.writeln('This text is in section 3.')
self.assertEqual(aw.SectionStart.CONTINUOUS, doc.sections[2].page_setup.section_start)
# 3 -  Commence la section suivante sur une nouvelle page paire:
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
builder.writeln('This text is in section 4.')
self.assertEqual(aw.SectionStart.EVEN_PAGE, doc.sections[3].page_setup.section_start)
# 4 -  Commence la section suivante sur une nouvelle page impaire:
builder.insert_break(aw.BreakType.SECTION_BREAK_ODD_PAGE)
builder.writeln('This text is in section 5.')
self.assertEqual(aw.SectionStart.ODD_PAGE, doc.sections[4].page_setup.section_start)
# 5 -  Commence la section suivante dans une nouvelle colonne:
columns = builder.page_setup.text_columns
columns.set_count(2)
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_COLUMN)
builder.writeln('This text is in section 6.')
self.assertEqual(aw.SectionStart.NEW_COLUMN, doc.sections[5].page_setup.section_start)
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.SetSectionStart.docx')
```

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

* module [aspose.words](../../)
* class [PageSetup](../)


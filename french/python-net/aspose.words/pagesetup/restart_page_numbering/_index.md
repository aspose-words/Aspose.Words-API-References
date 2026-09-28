---
title: PageSetup.restart_page_numbering property
linktitle: restart_page_numbering property
articleTitle: restart_page_numbering property
second_title: Aspose.Words for Python
description: "PageSetup.restart_page_numbering property. True if page numbering restarts at the beginning of the section."
type: docs
weight: 360
url: /fr/python-net/aspose.words/pagesetup/restart_page_numbering/
---

## PageSetup.restart_page_numbering property

True if page numbering restarts at the beginning of the section.


```python
@property
def restart_page_numbering(self) -> bool:
    ...

@restart_page_numbering.setter
def restart_page_numbering(self, value: bool):
    ...

```

### Remarks

If set to ``False``, the [PageSetup.restart_page_numbering](./) property will override the
[PageSetup.page_starting_number](../page_starting_number/) property so that page numbering can continue from the previous section.



### Examples

Shows how to set up page numbering in a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Section 1, page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 1, page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 1, page 3.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln('Section 2, page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 2, page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 2, page 3.')
# Déplacez le constructeur de document vers l'en-tête principal de la première section,
# qui sera affiché sur chaque page de cette section.
builder.move_to_section(0)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
# Insérez un champ PAGE, qui affichera le numéro de la page actuelle.
builder.write('Page ')
builder.insert_field(field_code='PAGE', field_value='')
# Configurez la section pour que le compteur de pages affiché par les champs PAGE commence à 5.
# De plus, configurez tous les champs PAGE pour afficher leurs numéros de page en chiffres romains majuscules.
page_setup = doc.sections[0].page_setup
page_setup.restart_page_numbering = True
page_setup.page_starting_number = 5
page_setup.page_number_style = aw.NumberStyle.UPPERCASE_ROMAN
# Créez un autre en-tête principal pour la deuxième section, avec un autre champ PAGE.
builder.move_to_section(1)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.write(' - ')
builder.insert_field(field_code='PAGE', field_value='')
builder.write(' - ')
# Configurez la section pour que le compteur de pages affiché par les champs PAGE commence à 10.
# De plus, configurez tous les champs PAGE pour afficher leurs numéros de page en chiffres arabes.
page_setup = doc.sections[1].page_setup
page_setup.page_starting_number = 10
page_setup.restart_page_numbering = True
page_setup.page_number_style = aw.NumberStyle.ARABIC
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PageNumbering.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)


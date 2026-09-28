---
title: FieldToc.preserve_line_breaks property
linktitle: preserve_line_breaks property
articleTitle: preserve_line_breaks property
second_title: Aspose.Words for Python
description: "FieldToc.preserve_line_breaks property. Gets or sets whether to preserve newline characters within table entries."
type: docs
weight: 130
url: /fr/python-net/aspose.words.fields/fieldtoc/preserve_line_breaks/
---

## FieldToc.preserve_line_breaks property

Gets or sets whether to preserve newline characters within table entries.


```python
@property
def preserve_line_breaks(self) -> bool:
    ...

@preserve_line_breaks.setter
def preserve_line_breaks(self, value: bool):
    ...

```

### Examples

Shows how to insert a TOC, and populate it with entries based on heading styles.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_bookmark('MyBookmark')
# Insérez un champ TOC, qui compilera tous les titres dans une table des matières.
# Pour chaque titre, ce champ créera une ligne avec le texte de ce style de titre à gauche,
# et la page où le titre apparaît à droite.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Utilisez la propriété BookmarkName pour ne répertorier que les titres
# qui apparaissent dans les limites d'un signet nommé "MyBookmark".
field.bookmark_name = 'MyBookmark'
# Le texte avec un style de titre intégré, tel que "Heading 1", appliqué, sera compté comme un titre.
# Nous pouvons nommer des styles supplémentaires à reconnaître comme titres par le TOC dans cette propriété et leurs niveaux TOC.
field.custom_styles = 'Quote; 6; Intense Quote; 7'
# Par défaut, les niveaux Styles/TOC sont séparés dans la propriété CustomStyles par une virgule,
# mais nous pouvons définir un délimiteur personnalisé dans cette propriété.
doc.field_options.custom_toc_style_separator = ';'
# Configurez le champ pour exclure tout titre dont les niveaux TOC sont en dehors de cette plage.
field.heading_level_range = '1-3'
# Le TOC n'affichera pas les numéros de page des titres dont les niveaux TOC sont dans cette plage.
field.page_number_omitting_level_range = '2-5'
# Définissez une chaîne personnalisée qui séparera chaque titre de son numéro de page.
field.entry_separator = '-'
field.insert_hyperlinks = True
field.hide_in_web_layout = False
field.preserve_line_breaks = True
field.preserve_tabs = True
field.use_paragraph_outline_level = False
self.insert_new_page_with_heading(builder, 'First entry', 'Heading 1')
builder.writeln('Paragraph text.')
self.insert_new_page_with_heading(builder, 'Second entry', 'Heading 1')
self.insert_new_page_with_heading(builder, 'Third entry', 'Quote')
self.insert_new_page_with_heading(builder, 'Fourth entry', 'Intense Quote')
# Ces deux titres auront les numéros de page omis car ils sont dans la plage "2-5".
self.insert_new_page_with_heading(builder, 'Fifth entry', 'Heading 2')
self.insert_new_page_with_heading(builder, 'Sixth entry', 'Heading 3')
# Cette entrée n'apparaît pas parce que "Heading 4" est en dehors de la plage "1-3" que nous avons définie précédemment.
self.insert_new_page_with_heading(builder, 'Seventh entry', 'Heading 4')
builder.end_bookmark('MyBookmark')
builder.writeln('Paragraph text.')
# Cette entrée n'apparaît pas car elle se trouve en dehors du signet spécifié par la table des matières.
self.insert_new_page_with_heading(builder, 'Eighth entry', 'Heading 1')
self.assertEqual(' TOC  \\b MyBookmark \\t "Quote; 6; Intense Quote; 7" \\o 1-3 \\n 2-5 \\p - \\h \\u0000 \\w', field.get_field_code())
field.update_page_numbers()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOC.docx')
```

Shows how to insert a TOC, and populate it with entries based on heading styles (InsertNewPageWithHeading).

```python
def insert_new_page_with_heading(self, builder, caption_text, style_name):
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    original_style = builder.paragraph_format.style_name
    builder.paragraph_format.style = builder.document.styles.get_by_name(style_name)
    builder.writeln(caption_text)
    builder.paragraph_format.style = builder.document.styles.get_by_name(original_style)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldToc](../)


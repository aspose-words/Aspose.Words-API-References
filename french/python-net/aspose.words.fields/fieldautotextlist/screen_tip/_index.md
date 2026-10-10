---
title: FieldAutoTextList.screen_tip property
linktitle: screen_tip property
articleTitle: screen_tip property
second_title: Aspose.Words for Python
description: "FieldAutoTextList.screen_tip property. Gets or sets the text of the ScreenTip to show."
type: docs
weight: 40
url: /fr/python-net/aspose.words.fields/fieldautotextlist/screen_tip/
---

## FieldAutoTextList.screen_tip property

Gets or sets the text of the ScreenTip to show.


```python
@property
def screen_tip(self) -> str:
    ...

@screen_tip.setter
def screen_tip(self, value: str):
    ...

```

### Examples

Shows how to use an AUTOTEXTLIST field to select from a list of AutoText entries.

```python
doc = aw.Document()
# Créez un document de glossaire et remplissez-le avec des entrées d'auto‑texte.
doc.glossary_document = aw.buildingblocks.GlossaryDocument()
ExField._append_auto_text_entry(doc.glossary_document, 'AutoText 1', 'Contents of AutoText 1')
ExField._append_auto_text_entry(doc.glossary_document, 'AutoText 2', 'Contents of AutoText 2')
ExField._append_auto_text_entry(doc.glossary_document, 'AutoText 3', 'Contents of AutoText 3')
builder = aw.DocumentBuilder(doc=doc)
# Créez un champ AUTOTEXTLIST et définissez le texte que le champ affichera dans Microsoft Word.
# Définissez le texte pour inviter l'utilisateur à faire un clic droit sur ce champ afin de sélectionner un bloc de construction AutoText,
# dont le contenu sera affiché par le champ.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_TEXT_LIST, update_field=True).as_field_auto_text_list()
field.entry_name = 'Right click here to select an AutoText block'
field.list_style = 'Heading 1'
field.screen_tip = 'Hover tip text for AutoTextList goes here'
self.assertEqual(' AUTOTEXTLIST  "Right click here to select an AutoText block" ' + '\\s "Heading 1" ' + '\\t "Hover tip text for AutoTextList goes here"', field.get_field_code())
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTOTEXTLIST.dotx')
```

Shows how to use an AUTOTEXTLIST field to select from a list of AutoText entries (AppendAutoTextEntry).

```python
@staticmethod
def _append_auto_text_entry(glossary_doc, name, contents):
    building_block = aw.buildingblocks.BuildingBlock(glossary_doc)
    building_block.name = name
    building_block.gallery = aw.buildingblocks.BuildingBlockGallery.AUTO_TEXT
    building_block.category = 'General'
    building_block.behavior = aw.buildingblocks.BuildingBlockBehavior.PARAGRAPH
    section = aw.Section(glossary_doc)
    section.append_child(aw.Body(glossary_doc))
    section.body.append_paragraph(contents)
    building_block.append_child(section)
    glossary_doc.append_child(building_block)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoTextList](../)


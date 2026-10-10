---
title: FieldAutoText.entry_name property
linktitle: entry_name property
articleTitle: entry_name property
second_title: Aspose.Words for Python
description: "FieldAutoText.entry_name property. Gets or sets the name of the AutoText entry."
type: docs
weight: 20
url: /de/python-net/aspose.words.fields/fieldautotext/entry_name/
---

## FieldAutoText.entry_name property

Gets or sets the name of the AutoText entry.


```python
@property
def entry_name(self) -> str:
    ...

@entry_name.setter
def entry_name(self, value: str):
    ...

```

### Examples

Shows how to display a building block with AUTOTEXT and GLOSSARY fields.

```python
doc = aw.Document()
# Erstellen Sie ein Glossar‑Dokument und fügen Sie ihm ein AutoText‑Baustein hinzu.
doc.glossary_document = aw.buildingblocks.GlossaryDocument()
building_block = aw.buildingblocks.BuildingBlock(doc.glossary_document)
building_block.name = 'MyBlock'
building_block.gallery = aw.buildingblocks.BuildingBlockGallery.AUTO_TEXT
building_block.category = 'General'
building_block.description = 'MyBlock description'
building_block.behavior = aw.buildingblocks.BuildingBlockBehavior.PARAGRAPH
doc.glossary_document.append_child(building_block)
# Erstellen Sie eine Quelle und fügen Sie sie als Text zu unserem Baustein hinzu.
building_block_source = aw.Document()
building_block_source_builder = aw.DocumentBuilder(doc=building_block_source)
building_block_source_builder.writeln('Hello World!')
building_block_content = doc.glossary_document.import_node(src_node=building_block_source.first_section, is_import_children=True)
building_block.append_child(building_block_content)
# Legen Sie eine Datei fest, die Teile enthält, die unser Dokument oder dessen angehängte Vorlage möglicherweise nicht enthält.
doc.field_options.built_in_templates_paths = [MY_DIR + 'Busniess brochure.dotx']
builder = aw.DocumentBuilder(doc=doc)
# Im Folgenden werden zwei Möglichkeiten gezeigt, Felder zu verwenden, um den Inhalt unseres Bausteins anzuzeigen.
# 1 -  Verwendung eines AUTOTEXT‑Feldes:
field_auto_text = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_TEXT, update_field=True).as_field_auto_text()
field_auto_text.entry_name = 'MyBlock'
self.assertEqual(' AUTOTEXT  MyBlock', field_auto_text.get_field_code())
# 2 -  Verwendung eines GLOSSARY-Feldes:
field_glossary = builder.insert_field(field_type=aw.fields.FieldType.FIELD_GLOSSARY, update_field=True).as_field_glossary()
field_glossary.entry_name = 'MyBlock'
self.assertEqual(' GLOSSARY  MyBlock', field_glossary.get_field_code())
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTOTEXT.GLOSSARY.dotx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoText](../)


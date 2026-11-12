---
title: IStructuredDocumentTag.placeholder_name property
linktitle: placeholder_name property
articleTitle: placeholder_name property
second_title: Aspose.Words for Python
description: "IStructuredDocumentTag.placeholder_name property. Gets or sets Name of the [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text."
type: docs
weight: 110
url: /tr/python-net/aspose.words.markup/istructureddocumenttag/placeholder_name/
---

## IStructuredDocumentTag.placeholder_name property

Gets or sets Name of the [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text.




```python
@property
def placeholder_name(self) -> str:
    ...

@placeholder_name.setter
def placeholder_name(self, value: str):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidOperationException)) | Throw if BuildingBlock with this name [BuildingBlock.name](../../../aspose.words.buildingblocks/buildingblock/name/) is not present in [Document.glossary_document](../../../aspose.words/document/glossary_document/). |

### Examples

Shows how to use a building block's contents as a custom placeholder text for a structured document tag.

```python
doc = aw.Document()
# "PlainText" türünde bir düz metin yapılandırılmış belge etiketi ekleyin; bu bir metin kutusu gibi çalışacaktır.
# Varsayılan olarak göstereceği içerik, "Metin girmek için buraya tıklayın." istemidir.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Etiketin varsayılan metin yerine bir yapı bloğunun içeriğini göstermesini sağlayabiliriz.
# İlk olarak, sözlük belgesine içerikli bir yapı bloğu ekleyin.
glossary_doc = doc.glossary_document
substitute_block = aw.buildingblocks.BuildingBlock(glossary_doc)
substitute_block.name = 'Custom Placeholder'
substitute_block.append_child(aw.Section(glossary_doc))
substitute_block.first_section.append_child(aw.Body(glossary_doc))
substitute_block.first_section.body.append_paragraph('Custom placeholder text.')
glossary_doc.append_child(substitute_block)
# Ardından, yapılandırılmış belge etiketinin "PlaceholderName" özelliğini kullanarak o yapı bloğunu adıyla referans alın.
tag.placeholder_name = 'Custom Placeholder'
# "PlaceholderName" üst belge'nin sözlük belgesindeki mevcut bir bloğa işaret ediyorsa,
# "Placeholder" özelliği aracılığıyla yapı bloğunu doğrulayabileceğiz.
self.assertEqual(substitute_block, tag.placeholder)
# "IsShowingPlaceholderText" özelliğini "true" olarak ayarlayarak
# yapılandırılmış belge etiketinin mevcut içeriğini yer tutucu metin olarak ele alın.
# Bu, Microsoft Word'de metin kutusuna tıklamanın etiketin tüm içeriğini hemen vurgulayacağı anlamına gelir.
# "IsShowingPlaceholderText" özelliğini "false" olarak ayarlayarak
# yapılandırılmış belge etiketinin içeriğini kullanıcının zaten girdiği metin olarak ele alın.
# Microsoft Word'de bu metne tıklamak, yanıp sönen imleci tıklanan konuma yerleştirecektir.
tag.is_showing_placeholder_text = is_showing_placeholder_text
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlaceholderBuildingBlock.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [IStructuredDocumentTag](../)


---
title: StructuredDocumentTag.id property
linktitle: id property
articleTitle: id property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.id property. Specifies a unique read-only persistent numerical Id for this SDT."
type: docs
weight: 140
url: /tr/python-net/aspose.words.markup/structureddocumenttag/id/
---

## StructuredDocumentTag.id property

Specifies a unique read-only persistent numerical Id for this **SDT**.




```python
@property
def id(self) -> int:
    ...

```

### Remarks

Id attribute shall follow these rules:

* The document shall retain SDT ids only if the whole document is cloned [Document.clone()](../../../aspose.words/document/clone/#bool).
  
* During [DocumentBase.import_node()](../../../aspose.words/documentbase/import_node/#node_bool)
  Id shall be retained if import does not cause conflicts with other SDT Ids in
  the target document.
  
* If multiple SDT nodes specify the same decimal number value for the Id attribute,
  then the first SDT in the document shall maintain this original Id,
  and all subsequent SDT nodes shall have new identifiers assigned to them when the document is loaded.
  
* During standalone SDT Aspose.Words.Markup.StructuredDocumentTag.Clone(System.Boolean,Aspose.Words.INodeCloningListener) operation new unique ID will be generated for the cloned SDT node.
  
* If Id is not specified in the source document, then the SDT node shall have a new unique identifier assigned
  to it when the document is loaded.
  





### Examples

Shows how to create a structured document tag in a plain text box and modify its appearance.

```python
doc = aw.Document()
# Düz metin içerecek bir yapılandırılmış belge etiketi oluşturun.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Microsoft Word'de yapılandırılmış belge etiketinin üzerine fareyle geldiğinizde görünen çerçevenin başlığını ve rengini ayarlayın.
tag.title = 'My plain text'
tag.color = aspose.pydrawing.Color.magenta
# Bu yapılandırılmış belge etiketi için, elde edilebilen bir etiket ayarlayın
# \"tag\" adlı bir XML öğesi olarak, aşağıdaki dizeyi "@val" özniteliğinde içerir.
tag.tag = 'MyPlainTextSDT'
# Her yapılandırılmış belge etiketinin rastgele benzersiz bir kimliği vardır.
self.assertTrue(tag.id > 0)
# Yapılandırılmış belge etiketi içindeki metnin yazı tipini ayarlayın.
tag.contents_font.name = 'Arial'
# Yapılandırılmış belge etiketinin sonundaki metnin yazı tipini ayarlayın.
# Ok tuşlarıyla etiketten çıktıktan sonra belge gövdesine yazdığımız tüm metin bu yazı tipini kullanacaktır.
tag.end_character_font.name = 'Arial Black'
# Varsayılan olarak, bu yanlıştır ve bir yapılandırılmış belge etiketi içinde Enter tuşuna basmak hiçbir şey yapmaz.
# Doğru olarak ayarlandığında, yapılandırılmış belge etiketimiz birden fazla satır içerebilir.
# \"Multiline\" özelliğini \"false\" olarak ayarlayın, yalnızca içeriğin
# bu yapılandırılmış belge etiketinin tek bir satırda yer almasını sağlamak için.
# \"Multiline\" özelliğini \"true\" olarak ayarlayın, etiketin birden fazla satır içerik içermesine izin vermek için.
tag.multiline = True
# \"Appearance\" özelliğini \"SdtAppearance.Tags\" olarak ayarlayın, içeriğin etrafında etiketleri göstermek için.
# Varsayılan olarak, yapılandırılmış belge etiketi BoundingBox olarak gösterilir.
tag.appearance = aw.markup.SdtAppearance.TAGS
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
# Yeni bir paragrafta yapılandırılmış belge etiketimizin bir kopyasını ekleyin.
tag_clone = tag.clone(True).as_structured_document_tag()
builder.insert_paragraph()
builder.insert_node(tag_clone)
# \"RemoveSelfOnly\" yöntemini kullanarak bir yapılandırılmış belge etiketini kaldırın, ancak içeriğini belgede tutun.
tag_clone.remove_self_only()
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlainText.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)


---
title: ParagraphFormat.left_indent property
linktitle: left_indent property
articleTitle: left_indent property
second_title: Aspose.Words for Python
description: "ParagraphFormat.left_indent property. Gets or sets the value (in points) that represents the left indent for paragraph."
type: docs
weight: 180
url: /tr/python-net/aspose.words/paragraphformat/left_indent/
---

## ParagraphFormat.left_indent property

Gets or sets the value (in points) that represents the left indent for paragraph.


```python
@property
def left_indent(self) -> float:
    ...

@left_indent.setter
def left_indent(self, value: float):
    ...

```

### Examples

Shows how to configure paragraph formatting to create off-center text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Belge oluşturucunun yazdığı tüm metni ortalayın ve girintileri ayarlayın.
# Aşağıdaki girinti yapılandırması, sayfada asimetrik olarak konumlanacak bir metin gövdesi oluşturacaktır.
# Metni hizaladığımız "merkez", sayfanın ortası değil, metin gövdesinin ortası olacaktır.
paragraph_format = builder.paragraph_format
paragraph_format.alignment = aw.ParagraphAlignment.CENTER
paragraph_format.left_indent = 100
paragraph_format.right_indent = 50
paragraph_format.space_after = 25
builder.writeln('This paragraph demonstrates how left and right indentation affects word wrapping.')
builder.writeln("The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.")
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SetParagraphFormatting.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)


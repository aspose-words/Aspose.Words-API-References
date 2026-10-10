---
title: ParagraphFormat.space_after property
linktitle: space_after property
articleTitle: space_after property
second_title: Aspose.Words for Python
description: "ParagraphFormat.space_after property. Gets or sets the amount of spacing (in points) after the paragraph."
type: docs
weight: 310
url: /tr/python-net/aspose.words/paragraphformat/space_after/
---

## ParagraphFormat.space_after property

Gets or sets the amount of spacing (in points) after the paragraph.


```python
@property
def space_after(self) -> float:
    ...

@space_after.setter
def space_after(self, value: float):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throws when argument was out of the range of valid values. |

### Remarks

Has no effect when [ParagraphFormat.space_after_auto](../space_after_auto/) is ``True``.

Valid values ​​range from 0 to 1584 inclusive.




### Examples

Shows how to set automatic paragraph spacing.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Bu oluşturucunun oluşturacağı paragrafların önüne ve arkasına büyük miktarda boşluk uygulayın.
builder.paragraph_format.space_before = 24
builder.paragraph_format.space_after = 24
# Otomatik boşluk uygulamak için bu bayrakları "true" olarak ayarlayın,
# yukarıda ayarladığımız özelliklerdeki boşlukları etkili bir şekilde yok sayarak.
# Onları "false" bırakmak, özel paragraf boşluklamamızı uygular.
builder.paragraph_format.space_after_auto = auto_spacing
builder.paragraph_format.space_before_auto = auto_spacing
# Üstünde ve altında boşluk olacak iki paragraf ekleyin ve belgeyi kaydedin.
builder.writeln('Paragraph 1.')
builder.writeln('Paragraph 2.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphSpacingAuto.docx')
```

Shows how to apply no spacing between paragraphs with the same style.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Bu oluşturucunun oluşturacağı paragrafların önüne ve arkasına büyük miktarda boşluk uygulayın.
builder.paragraph_format.space_before = 24
builder.paragraph_format.space_after = 24
# "NoSpaceBetweenParagraphsOfSameStyle" bayrağını "true" olarak ayarlayarak uygulayın
# aynı stile sahip paragraflar arasında boşluk bırakmayarak benzer paragrafları gruplayacaktır.
# "NoSpaceBetweenParagraphsOfSameStyle" bayrağını "false" olarak bırakın
# her paragraf için boşluğu eşit şekilde uygulamak için.
builder.paragraph_format.no_space_between_paragraphs_of_same_style = no_space_between_paragraphs_of_same_style
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.paragraph_format.style = doc.styles.get_by_name('Quote')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphSpacingSameStyle.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)


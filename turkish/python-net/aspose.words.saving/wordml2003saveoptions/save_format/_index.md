---
title: WordML2003SaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "WordML2003SaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 20
url: /tr/python-net/aspose.words.saving/wordml2003saveoptions/save_format/
---

## WordML2003SaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.WORD_ML](../../../aspose.words/saveformat/#WORD_ML).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to manage output document's raw content.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# "WordML2003SaveOptions" nesnesi oluşturun ve belge'nin "Save" yöntemine geçirin
# belgeyi WordML kaydetme formatına nasıl kaydedeceğimizi değiştirmek için
options = aw.saving.WordML2003SaveOptions()
self.assertEqual(aw.SaveFormat.WORD_ML, options.save_format)
# "PrettyFormat" özelliğini "true" olarak ayarlayın, sekme karakteri girintisi ve
# satır sonlarını ekleyerek çıktı belgesinin ham içeriğini daha kolay okunur hâle getirin.
# "PrettyFormat" özelliğini "false" olarak ayarlayın, belge'nin ham içeriğini tek bir sürekli metin bloğu olarak kaydedin.
options.pretty_format = pretty_format
doc.save(file_name=ARTIFACTS_DIR + 'WordML2003SaveOptions.PrettyFormat.xml', save_options=options)
file_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'WordML2003SaveOptions.PrettyFormat.xml')
new_line = system_helper.environment.Environment.new_line()
if pretty_format:
    self.assertTrue(f'<o:DocumentProperties>{new_line}\t\t' + f'<o:Revision>1</o:Revision>{new_line}\t\t' + f'<o:TotalTime>0</o:TotalTime>{new_line}\t\t' + f'<o:Pages>1</o:Pages>{new_line}\t\t' + f'<o:Words>0</o:Words>{new_line}\t\t' + f'<o:Characters>0</o:Characters>{new_line}\t\t' + f'<o:Lines>1</o:Lines>{new_line}\t\t' + f'<o:Paragraphs>1</o:Paragraphs>{new_line}\t\t' + f'<o:CharactersWithSpaces>0</o:CharactersWithSpaces>{new_line}\t\t' + f'<o:Version>11.5606</o:Version>{new_line}\t' + '</o:DocumentProperties>' in file_contents)
else:
    self.assertTrue('<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>' + '<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>' + '<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>' in file_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [WordML2003SaveOptions](../)


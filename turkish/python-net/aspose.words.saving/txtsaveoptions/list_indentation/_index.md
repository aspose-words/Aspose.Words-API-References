---
title: TxtSaveOptions.list_indentation property
linktitle: list_indentation property
articleTitle: list_indentation property
second_title: Aspose.Words for Python
description: "TxtSaveOptions.list_indentation property. Gets a [TxtListIndentation](../../txtlistindentation/) object that specifies how many and which character to use for indentation of list levels"
type: docs
weight: 30
url: /tr/python-net/aspose.words.saving/txtsaveoptions/list_indentation/
---

## TxtSaveOptions.list_indentation property

Gets a [TxtListIndentation](../../txtlistindentation/) object that specifies how many and which character to use for indentation of list levels.
By default, it is zero count of character '\\0', that means no indentation.



```python
@property
def list_indentation(self) -> aspose.words.saving.TxtListIndentation:
    ...

```

### Examples

Shows how to configure list indenting when saving a document to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Üç seviyeli girintiye sahip bir liste oluşturun.
builder.list_format.apply_number_default()
builder.writeln('Item 1')
builder.list_format.list_indent()
builder.writeln('Item 2')
builder.list_format.list_indent()
builder.write('Item 3')
# "TxtSaveOptions" nesnesi oluşturun, bunu belgenin "Save" metoduna geçirebiliriz
# belgeyi düz metin olarak nasıl kaydedeceğimizi değiştirmek için.
txt_save_options = aw.saving.TxtSaveOptions()
# "Character" özelliğini, kullanılacak bir karakter atamak için ayarlayın
# düz metinde liste girintisini taklit eden doldurma için.
txt_save_options.list_indentation.character = ' '
# "Count" özelliğini, kaç kez olduğunu belirtmek için ayarlayın
# her liste girinti seviyesi için doldurma karakterini yerleştirmek amacıyla.
txt_save_options.list_indentation.count = 3
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.TxtListIndentation.txt', save_options=txt_save_options)
doc_text = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'TxtSaveOptions.TxtListIndentation.txt')
new_line = system_helper.environment.Environment.new_line()
self.assertEqual(f'1. Item 1{new_line}' + f'   a. Item 2{new_line}' + f'      i. Item 3{new_line}', doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptions](../)


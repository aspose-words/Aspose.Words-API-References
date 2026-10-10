---
title: PageExtractOptions.update_page_starting_number property
linktitle: update_page_starting_number property
articleTitle: update_page_starting_number property
second_title: Aspose.Words for Python
description: "PageExtractOptions.update_page_starting_number property. Specifies whether the start page number in the resulting document shall be updated"
type: docs
weight: 30
url: /zh/python-net/aspose.words/pageextractoptions/update_page_starting_number/
---

## PageExtractOptions.update_page_starting_number property

Specifies whether the start page number in the resulting document shall be updated.
Default value is ``True``.



```python
@property
def update_page_starting_number(self) -> bool:
    ...

@update_page_starting_number.setter
def update_page_starting_number(self, value: bool):
    ...

```

### Examples

Show how to reset the initial page numbering and save the NUMPAGE field.

```python
doc = aw.Document(file_name=MY_DIR + 'Page fields.docx')
# 默认行为：
# 提取的页码与原始文档相同，就好像我们在 MS Word 中选择了 "Print 2 pages"。
# 起始页将设置为 2，指示页数的字段将被移除
# 并替换为等于页数的常量值。
extracted_doc1 = doc.extract_pages(index=1, count=1)
extracted_doc1.save(file_name=ARTIFACTS_DIR + 'Document.ExtractPagesWithOptions.Default.docx')
# 更改后的行为：
# 提取的页码被重置，新的页码开始，
# 就好像我们复制了第二页的内容并粘贴到新文档中。
# 起始页将设置为 1，指示页数的字段将保持不变
# 并将显示当前的页数。
extract_options = aw.PageExtractOptions()
extract_options.update_page_starting_number = False
extract_options.unlink_pages_number_fields = False
extracted_doc2 = doc.extract_pages(index=1, count=1, options=extract_options)
extracted_doc2.save(file_name=ARTIFACTS_DIR + 'Document.ExtractPagesWithOptions.Options.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageExtractOptions](../)


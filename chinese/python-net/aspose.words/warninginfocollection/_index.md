---
title: WarningInfoCollection class
linktitle: WarningInfoCollection class
articleTitle: WarningInfoCollection class
second_title: Aspose.Words for Python
description: "aspose.words.WarningInfoCollection class. Represents a typed collection of [WarningInfo](../warninginfo/) objects"
type: docs
weight: 1460
url: /zh/python-net/aspose.words/warninginfocollection/
---

## WarningInfoCollection class

Represents a typed collection of [WarningInfo](../warninginfo/) objects.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/python-net/programming-with-documents/) documentation article.




### Remarks

You can use this collection object as the simplest form of [IWarningCallback](../iwarningcallback/) implementation to gather 
all warnings that Aspose.Words generates during a load or save operation. Create an instance of this class and assign it 
to the [LoadOptions.warning_callback](../../aspose.words.loading/loadoptions/warning_callback/) or [DocumentBase.warning_callback](../documentbase/warning_callback/) property.




**Interfaces:** [IWarningCallback](../iwarningcallback/)

### Constructors
| Name | Description |
| --- | --- |
| [WarningInfoCollection()](./__init__/#default) | The default constructor. |

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets an item at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of elements contained in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ clear()](./clear/#default) | Removes all elements from the collection. |
|[ warning(info)](./warning/#warninginfo) | Implements the [IWarningCallback](../iwarningcallback/) interface. Adds a warning to this collection. |

### Examples

Shows how to set the property for finding the closest match for a missing font from the available font sources.

```python
# 打开一个文档，其中包含使用我们任何字体源中不存在的字体格式化的文本。
doc = aw.Document(file_name=MY_DIR + 'Missing font.docx')
# 为处理字体替换警告分配回调函数。
warning_collector = aw.WarningInfoCollection()
doc.warning_callback = warning_collector
# 设置默认字体名称并启用字体替换。
font_settings = aw.fonts.FontSettings()
font_settings.substitution_settings.default_font_substitution.default_font_name = 'Arial'
font_settings.substitution_settings.font_info_substitution.enabled = True
# 字体替换后应使用原始字体度量。
doc.layout_options.keep_original_font_metrics = True
# 如果我们保存的文档缺少字体，将会收到字体替换警告。
doc.font_settings = font_settings
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.EnableFontSubstitution.pdf')
for info in warning_collector:
    if info.warning_type == aw.WarningType.FONT_SUBSTITUTION:
        print(info.description)
```

### See Also

* module [aspose.words](../)
* class [IWarningCallback](../iwarningcallback/)
* class [WarningInfo](../warninginfo/)


---
title: HtmlLoadOptions.web_request_timeout property
linktitle: web_request_timeout property
articleTitle: web_request_timeout property
second_title: Aspose.Words for Python
description: "HtmlLoadOptions.web_request_timeout property. The number of milliseconds to wait before the web request times out"
type: docs
weight: 80
url: /zh/python-net/aspose.words.loading/htmlloadoptions/web_request_timeout/
---

## HtmlLoadOptions.web_request_timeout property

The number of milliseconds to wait before the web request times out. The default value is 100000 milliseconds
(100 seconds).


```python
@property
def web_request_timeout(self) -> int:
    ...

@web_request_timeout.setter
def web_request_timeout(self, value: int):
    ...

```

### Remarks

The number of milliseconds that Aspose.Words waits for a response, when loading external resources (images, style
sheets) linked in HTML and MHTML documents.


### Examples

Shows how to set a time limit for web requests when loading a document with external resources linked by URLs.

```python
image_uri = 'https://samplelib.com/png/sample-alpha-circle-400x300.png'
# 创建一个新的 HtmlLoadOptions 对象并验证其网页请求的超时阈值。
options = aw.loading.HtmlLoadOptions()
# 在加载通过网页地址 URL 外部链接资源的 Html 文档时，
# Aspose.Words 将中止在此时间限制（毫秒）内未能获取资源的网页请求。
self.assertEqual(100000, options.web_request_timeout)
# 设置一个 WarningCallback，以记录加载期间出现的所有警告。
warning_callback = self.ListDocumentWarnings()
options.warning_callback = warning_callback
# 加载此类文档并验证已创建包含图像数据的形状。
# 此链接图像需要进行网络请求才能加载，且必须在我们的时间限制内完成。
html = f'\n        <html>\n        <img src=""{image_uri}"" alt=""Aspose logo"" style=""width:400px;height:400px;"">\n        </html>\n        '
# 设置一个不合理的超时时间限制，然后再次尝试加载文档。
options.web_request_timeout = 0
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(html, system_helper.text.Encoding.utf_8())), load_options=options)
self.assertEqual(2, len(warning_callback.warnings()))
# 即使网络请求未能在时间限制内获取图像，仍会生成一张图像。
# 然而，该图像将是常用来表示缺失图像的红色 “x”。
image_shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
self.assertEqual(924, len(image_shape.image_data.image_bytes))
# 我们还可以配置自定义回调，以捕获超时网络请求产生的任何警告。
self.assertEqual(aw.loading.WarningSource.HTML, warning_callback.warnings()[0].source)
self.assertEqual(aw.loading.WarningType.DATA_LOSS, warning_callback.warnings()[0].warning_type)
self.assertEqual(f"Couldn't load a resource from '{image_uri}'.", warning_callback.warnings()[0].description)
self.assertEqual(aw.loading.WarningSource.HTML, warning_callback.warnings()[1].source)
self.assertEqual(aw.loading.WarningType.DATA_LOSS, warning_callback.warnings()[1].warning_type)
self.assertEqual('Image has been replaced with a placeholder.', warning_callback.warnings()[1].description)
doc.save(file_name=ARTIFACTS_DIR + 'HtmlLoadOptions.WebRequestTimeout.docx')
```

Shows how to set a time limit for web requests when loading a document with external resources linked by URLs (ListDocumentWarnings).

```python
class ListDocumentWarnings(aw.IWarningCallback):

    def __init__(self):
        self.m_warnings = []

    def warning(self, info):
        self.m_warnings.append(info)

    def warnings(self):
        return self.m_warnings
```

### See Also

* module [aspose.words.loading](../../)
* class [HtmlLoadOptions](../)


﻿---
title: CssSavingArgs class
linktitle: CssSavingArgs class
articleTitle: CssSavingArgs class
second_title: Aspose.Words for Python
description: "aspose.words.saving.CssSavingArgs class. Provides data for the [ICssSavingCallback.css_saving()](../icsssavingcallback/css_saving/#csssavingargs) event"
type: docs
weight: 40
url: /python-net/aspose.words.saving/csssavingargs/
---

## CssSavingArgs class

Provides data for the [ICssSavingCallback.css_saving()](../icsssavingcallback/css_saving/#csssavingargs) event.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/python-net/save-a-document/) documentation article.




By default, when Aspose.Words saves a document to HTML, it saves CSS information inline
(as a value of the **style** attribute on every element).


[CssSavingArgs](./) allows to save CSS information into file by providing your own stream object.

To save CSS into stream, use the [CssSavingArgs.css_stream](./css_stream/) property.

To suppress saving CSS into a file and embedding to HTML document use the [CssSavingArgs.is_export_needed](./is_export_needed/) property.




### Properties

| Name | Description |
| --- | --- |
| [css_stream](./css_stream/) | Allows to specify the stream where the CSS information will be saved to. |
| [document](./document/) | Gets the document object that is currently being saved. |
| [is_export_needed](./is_export_needed/) | Allows to specify whether the CSS will be exported to file and embedded to HTML document. Default is ``True``. When this property is ``False``, the CSS information will not be saved to a CSS file and will not be embedded to HTML document. |
| [keep_css_stream_open](./keep_css_stream_open/) | Specifies whether Aspose.Words should keep the stream open or close it after saving an CSS information. |

### See Also

* module [aspose.words.saving](../)


---
title: Watermark.setText method
linktitle: setText method
articleTitle: setText method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Watermark.setText method"
type: docs
weight: 40
url: /nodejs-net/Aspose.Words/watermark/setText/
---

## setText(text) {#string}

Adds Text watermark into the document.


```js
setText(text: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | string | Text that is displayed as a watermark. |

### Remarks

The text length must be in the range from 1 to 200 inclusive.
The text cannot be ``null`` or contain only whitespaces.



### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throws when the text length is out of range or the text contains only whitespaces. |
| RuntimeError (Proxy error(ArgumentNullException)) | Throws when the text is ``null``. |

## setText(text, options) {#string_textwatermarkoptions}

Adds Text watermark into the document.


```js
setText(text: stringoptions: Aspose.Words.TextWatermarkOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | string | Text that is displayed as a watermark. |
| options | [TextWatermarkOptions](../../textwatermarkoptions/) | Defines additional options for the text watermark. |

### Remarks

The text length must be in the range from 1 to 200 inclusive.
The text cannot be ``null`` or contain only whitespaces.



If [TextWatermarkOptions](../../textwatermarkoptions/) is ``null``, the watermark will be set with default options.


### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throws when the text length is out of range or the text contain only whitespaces. |
| RuntimeError (Proxy error(ArgumentNullException)) | Throws when the text is ``null``. |

## See Also

* module [Aspose.Words](../../)
* class [Watermark](../)


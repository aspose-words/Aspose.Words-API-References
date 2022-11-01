---
title: warning_callback property
second_title: Aspose.Words for Python via .NET API Reference
description: "Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss."
type: docs
weight: 80
url: /python-net/aspose.words/documentbase/warning_callback/
---

## DocumentBase.warning_callback property

Called during various document processing procedures when an issue is detected that might result
in data or formatting fidelity loss.

Document may generate warnings at any stage of its existence, so it's important to setup warning callback as
early as possible to avoid the warnings loss. E.g. such properties as [Document.page_count](../../document/page_count/)
actually build the document layout which is used later for rendering, and the layout warnings may be lost if
warning callback is specified just for the rendering calls later.



### See Also

* module [aspose.words](../../)
* class [DocumentBase](../)


---
title: original_file_name property
second_title: Aspose.Words for Python via .NET API Reference
description: "The name of the CHM file"
type: docs
weight: 20
url: /python-net/aspose.words.loading/chmloadoptions/original_file_name/
---

## ChmLoadOptions.original_file_name property

The name of the CHM file.
Default value is ``null``.


CHM documents may contain links that reference the same document by file name. Aspose.Words supports such links
and normally uses [Document.original_file_name](../../../aspose.words/document/original_file_name/) to check whether the file referenced by a link
is the file that is being loaded. If a document is loaded from a stream, its original file name should be specified
explicitly via this property, since it cannot be determined automatically.


If a CHM document is loaded from a file and a non-null value for this property is specified, the value will take
priority over the actual name of the file stored in [Document.original_file_name](../../../aspose.words/document/original_file_name/).





### See Also

* module [aspose.words.loading](../../)
* class [ChmLoadOptions](../)


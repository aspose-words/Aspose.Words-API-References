---
title: get_OriginalFileName
second_title: Aspose.Words for C++ API Reference
description: The name of the CHM file. Default value is null.
type: docs
weight: 27
url: /cpp/aspose.words.loading/chmloadoptions/get_originalfilename/
---
## ChmLoadOptions::get_OriginalFileName method


The name of the CHM file. Default value is **null**.

```cpp
System::String Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName() const
```

## Remarks


CHM documents may contain links that reference the same document by file name. Aspose.Words supports such links and normally uses [OriginalFileName](../../../aspose.words/document/get_originalfilename/) to check whether the file referenced by a link is the file that is being loaded. If a document is loaded from a stream, its original file name should be specified explicitly via this property, since it cannot be determined automatically.

If a CHM document is loaded from a file and a non-null value for this property is specified, the value will take priority over the actual name of the file stored in [OriginalFileName](../../../aspose.words/document/get_originalfilename/). 
## See Also

* Class [ChmLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words](../../../)

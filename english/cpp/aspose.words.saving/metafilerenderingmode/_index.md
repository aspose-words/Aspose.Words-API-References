---
title: Aspose::Words::Saving::MetafileRenderingMode enum
linktitle: MetafileRenderingMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MetafileRenderingMode enum. Specifies how Aspose.Words should render WMF and EMF metafiles in C++.'
type: docs
weight: 69000
url: /cpp/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enum


Specifies how Aspose.Words should render WMF and EMF metafiles.

```cpp
enum class MetafileRenderingMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| VectorWithFallback | 0 | Aspose.Words tries to render a metafile as vector graphics. If Aspose.Words cannot correctly render some of the metafile records to vector graphics then Aspose.Words renders this metafile to a bitmap. |
| Vector | 1 | Aspose.Words renders a metafile as vector graphics. |
| Bitmap | 2 | Aspose.Words invokes GDI+ to render a metafile to a bitmap and then saves the bitmap to the output document. |

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)

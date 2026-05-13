---
title: Aspose::Words::ImportFormatOptions::get_ResolveThemeColors method
linktitle: get_ResolveThemeColors
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ImportFormatOptions::get_ResolveThemeColors method. Gets or sets a boolean value that specifies whether to resolve theme colors of the shapes forcibly. The default value is false in C++.'
type: docs
weight: 8500
url: /cpp/aspose.words/importformatoptions/get_resolvethemecolors/
---
## ImportFormatOptions::get_ResolveThemeColors method


Gets or sets a boolean value that specifies whether to resolve theme colors of the shapes forcibly. The default value is **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ResolveThemeColors() const
```

## Remarks


Please note that this option is only relevant for the [KeepSourceFormatting](../../importformatmode/) mode.

Normally, Aspose.Words doesn't resolve source theme colors when importing styles can be preserved without expanding formatting attributes into direct ones. However, in this case the actual colors of the imported shapes can differ from the ones they had in the original document. The reason for this is the different theme colors in the source and destination documents. Setting this option to **true** forces to resolve source shape theme colors and hence to preserve the actual color of the shapes they have in the source document. 
## See Also

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

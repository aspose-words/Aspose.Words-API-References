---
title: Aspose::Words::Shading::get_BackgroundTintAndShade method
linktitle: get_BackgroundTintAndShade
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Shading::get_BackgroundTintAndShade method. Gets or sets a double value that lightens or darkens a background theme color in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words/shading/get_backgroundtintandshade/
---
## Shading::get_BackgroundTintAndShade method


Gets or sets a double value that lightens or darkens a background theme color.

```cpp
double Aspose::Words::Shading::get_BackgroundTintAndShade()
```

## Remarks


The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in [ArgumentOutOfRangeException](../).

Setting this property for [Shading](../) object with non-theme colors results in [InvalidOperationException](../). 
## See Also

* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

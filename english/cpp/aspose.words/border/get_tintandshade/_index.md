---
title: get_TintAndShade
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a double value that lightens or darkens a color.
type: docs
weight: 131
url: /cpp/aspose.words/border/get_tintandshade/
---
## Border::get_TintAndShade method


Gets or sets a double value that lightens or darkens a color.

```cpp
double Aspose::Words::Border::get_TintAndShade()
```

## Remarks


The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in [ArgumentOutOfRangeException](../).

Setting this property for [Border](../) object with non-theme colors results in [InvalidOperationException](../). 
## See Also

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)

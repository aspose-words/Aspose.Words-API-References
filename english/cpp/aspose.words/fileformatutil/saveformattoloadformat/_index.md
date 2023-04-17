---
title: Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat method
linktitle: SaveFormatToLoadFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat method. Converts a SaveFormat value to a LoadFormat value if possible in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil::SaveFormatToLoadFormat method


Converts a [SaveFormat](../../saveformat/) value to a [LoadFormat](../../loadformat/) value if possible.

```cpp
static Aspose::Words::LoadFormat Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat saveFormat)
```


## Examples



Shows how to convert a save format to its corresponding load format. 
```cpp
ASSERT_EQ(LoadFormat::Html, FileFormatUtil::SaveFormatToLoadFormat(SaveFormat::Html));

// Some file types can have documents saved to, but not loaded from using Aspose.Words.
// If we attempt to convert a save format of such a type to a load format, an exception will be thrown.
ASSERT_THROW(FileFormatUtil::SaveFormatToLoadFormat(SaveFormat::Jpeg), System::ArgumentException);
```

## See Also

* Enum [LoadFormat](../../loadformat/)
* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

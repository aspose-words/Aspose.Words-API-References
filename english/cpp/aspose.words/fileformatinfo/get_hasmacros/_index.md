---
title: Aspose::Words::FileFormatInfo::get_HasMacros method
linktitle: get_HasMacros
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::FileFormatInfo::get_HasMacros method. Returns true if this document contains a VBA macros in C++.'
type: docs
weight: 3500
url: /cpp/aspose.words/fileformatinfo/get_hasmacros/
---
## FileFormatInfo::get_HasMacros method


Returns **true** if this document contains a VBA macros.

```cpp
bool Aspose::Words::FileFormatInfo::get_HasMacros() const
```


## Examples



Shows how to check VBA macro presence without loading document. 
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> fileFormatInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Macro.docm");
ASSERT_TRUE(fileFormatInfo->get_HasMacros());
```

## See Also

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

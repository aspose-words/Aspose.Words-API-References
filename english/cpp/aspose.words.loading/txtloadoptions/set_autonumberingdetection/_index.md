---
title: Aspose::Words::Loading::TxtLoadOptions::set_AutoNumberingDetection method
linktitle: set_AutoNumberingDetection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::TxtLoadOptions::set_AutoNumberingDetection method. Sets a boolean value indicating either automatic numbering detection will be performed while loading a document. The default value is true in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.loading/txtloadoptions/set_autonumberingdetection/
---
## TxtLoadOptions::set_AutoNumberingDetection method


Sets a boolean value indicating either automatic numbering detection will be performed while loading a document. The default value is **true**.

```cpp
void Aspose::Words::Loading::TxtLoadOptions::set_AutoNumberingDetection(bool value)
```

## Examples


Shows how to disable automatic numbering detection.

```cpp
auto options = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
options->set_AutoNumberingDetection(false);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Number detection.txt", options);
```
## See Also

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)

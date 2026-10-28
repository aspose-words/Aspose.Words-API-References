---
title: Aspose::Words::Loading::LoadOptions::set_IgnoreOleData method
linktitle: set_IgnoreOleData
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::LoadOptions::set_IgnoreOleData method. Specifies whether to ignore the OLE data in C++.'
type: docs
weight: 26000
url: /cpp/aspose.words.loading/loadoptions/set_ignoreoledata/
---
## LoadOptions::set_IgnoreOleData method


Specifies whether to ignore the OLE data.

```cpp
void Aspose::Words::Loading::LoadOptions::set_IgnoreOleData(bool value)
```

## Remarks


Ignoring OLE data may reduce memory consumption and increase performance without data lost in a case when destination format does not support OLE objects.

The default value is **false**.
## Examples


Shows how to ingore OLE data while loading.

```cpp
// Ignoring OLE data may reduce memory consumption and increase performance
// without data lost in a case when destination format does not support OLE objects.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_IgnoreOleData(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE objects.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.IgnoreOleData.docx");
```
## See Also

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)

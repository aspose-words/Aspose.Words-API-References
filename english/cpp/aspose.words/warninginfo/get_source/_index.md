---
title: Aspose::Words::WarningInfo::get_Source method
linktitle: get_Source
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::WarningInfo::get_Source method. Returns the source of the warning in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/warninginfo/get_source/
---
## WarningInfo::get_Source method


Returns the source of the warning.

```cpp
Aspose::Words::WarningSource Aspose::Words::WarningInfo::get_Source() const
```


## Examples



Shows how to work with the warning source. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Emphases markdown warning.docx");

auto warnings = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warnings);
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.EmphasesWarningSourceMarkdown.md");

for (auto&& warningInfo : warnings)
{
    if (warningInfo->get_Source() == Aspose::Words::WarningSource::Markdown)
    {
        ASSERT_EQ(u"The (*, 0:11) cannot be properly written into Markdown.", warningInfo->get_Description());
    }
}
```

## See Also

* Enum [WarningSource](../../warningsource/)
* Class [WarningInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

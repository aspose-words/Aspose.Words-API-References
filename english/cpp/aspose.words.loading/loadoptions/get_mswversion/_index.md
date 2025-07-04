---
title: Aspose::Words::Loading::LoadOptions::get_MswVersion method
linktitle: get_MswVersion
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::LoadOptions::get_MswVersion method. Allows to specify that the document loading process should match a specific MS Word version. Default value is Word2019 in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.loading/loadoptions/get_mswversion/
---
## LoadOptions::get_MswVersion method


Allows to specify that the document loading process should match a specific MS Word version. Default value is [Word2019](../../../aspose.words.settings/mswordversion/)

```cpp
Aspose::Words::Settings::MsWordVersion Aspose::Words::Loading::LoadOptions::get_MswVersion() const
```


## Examples



Shows how to emulate the loading procedure of a specific Microsoft Word version during document loading. 
```cpp
// By default, Aspose.Words load documents according to Microsoft Word 2019 specification.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

ASSERT_EQ(Aspose::Words::Settings::MsWordVersion::Word2019, loadOptions->get_MswVersion());

// This document is missing the default paragraph formatting style.
// This default style will be regenerated when we load the document either with Microsoft Word or Aspose.Words.
loadOptions->set_MswVersion(Aspose::Words::Settings::MsWordVersion::Word2007);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

// The style's line spacing will have this value when loaded by Microsoft Word 2007 specification.
ASSERT_NEAR(12.95, doc->get_Styles()->get_DefaultParagraphFormat()->get_LineSpacing(), 0.01);
```

## See Also

* Enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)

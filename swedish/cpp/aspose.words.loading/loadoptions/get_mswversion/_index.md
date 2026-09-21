---
title: "Aspose::Words::Loading::LoadOptions::get_MswVersion metod"
linktitle: "get_MswVersion"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::LoadOptions::get_MswVersion metod. Tillåter att ange att dokumentladdningsprocessen ska matcha en specifik MS Word-version. Standardvärdet är Word2019 i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.loading/loadoptions/get_mswversion/
---
## LoadOptions::get_MswVersion method


Tillåter att ange att dokumentladdningsprocessen ska matcha en specifik MS Word-version. Standardvärdet är [Word2019](../../../aspose.words.settings/mswordversion/)

```cpp
Aspose::Words::Settings::MsWordVersion Aspose::Words::Loading::LoadOptions::get_MswVersion() const
```


## Exempel



Visar hur man emulerar laddningsproceduren för en specifik Microsoft Word-version under dokumentladdning.
```cpp
// Som standard laddar Aspose.Words dokument enligt Microsoft Word 2019-specifikationen.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

ASSERT_EQ(Aspose::Words::Settings::MsWordVersion::Word2019, loadOptions->get_MswVersion());

// Detta dokument saknar standardformatmall för stycke.
// Denna standardstil kommer att återskapas när vi laddar dokumentet antingen med Microsoft Word eller Aspose.Words.
loadOptions->set_MswVersion(Aspose::Words::Settings::MsWordVersion::Word2007);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

// Stilens radavstånd kommer att ha detta värde när det laddas enligt Microsoft Word 2007-specifikationen.
ASSERT_NEAR(12.95, doc->get_Styles()->get_DefaultParagraphFormat()->get_LineSpacing(), 0.01);
```

## Se även

* Enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)

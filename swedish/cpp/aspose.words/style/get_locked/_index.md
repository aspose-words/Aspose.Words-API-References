---
title: "Aspose::Words::Style::get_Locked metod"
linktitle: "get_Locked"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Style::get_Locked metod. Anger om denna stil är låst i C++."
type: docs
weight: 13500
url: /sv/cpp/aspose.words/style/get_locked/
---
## Style::get_Locked method


Anger om denna stil är låst.

```cpp
bool Aspose::Words::Style::get_Locked() const
```


## Exempel



Visar hur man låser en stil.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> styleHeading1 = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1);
if (!styleHeading1->get_Locked())
{
    styleHeading1->set_Locked(true);
}

doc->Save(get_ArtifactsDir() + u"Styles.LockStyle.docx");
```

## Se även

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

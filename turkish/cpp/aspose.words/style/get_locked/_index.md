---
title: "Aspose::Words::Style::get_Locked yöntemi"
linktitle: "get_Locked"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Style::get_Locked yöntemi. Bu stilin C++'ta kilitli olup olmadığını belirtir."
type: docs
weight: 13500
url: /tr/cpp/aspose.words/style/get_locked/
---
## Style::get_Locked method


Bu stilin kilitli olup olmadığını belirtir.

```cpp
bool Aspose::Words::Style::get_Locked() const
```


## Örnekler



Stilin nasıl kilitleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> styleHeading1 = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1);
if (!styleHeading1->get_Locked())
{
    styleHeading1->set_Locked(true);
}

doc->Save(get_ArtifactsDir() + u"Styles.LockStyle.docx");
```

## Ayrıca Bakınız

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

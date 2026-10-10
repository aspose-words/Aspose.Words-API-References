---
title: "Aspose::Words::Style::get_Locked Methode"
linktitle: "get_Locked"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Style::get_Locked Methode. Gibt an, ob dieser Stil in C++ gesperrt ist."
type: docs
weight: 13500
url: /de/cpp/aspose.words/style/get_locked/
---
## Style::get_Locked method


Gibt an, ob dieser Stil gesperrt ist.

```cpp
bool Aspose::Words::Style::get_Locked() const
```


## Beispiele



Zeigt, wie man einen Stil sperrt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> styleHeading1 = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1);
if (!styleHeading1->get_Locked())
{
    styleHeading1->set_Locked(true);
}

doc->Save(get_ArtifactsDir() + u"Styles.LockStyle.docx");
```

## Siehe auch

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

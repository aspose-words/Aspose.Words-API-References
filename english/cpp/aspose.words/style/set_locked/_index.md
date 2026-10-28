---
title: Aspose::Words::Style::set_Locked method
linktitle: set_Locked
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Style::set_Locked method. Specifies whether this style is locked in C++.'
type: docs
weight: 25500
url: /cpp/aspose.words/style/set_locked/
---
## Style::set_Locked method


Specifies whether this style is locked.

```cpp
void Aspose::Words::Style::set_Locked(bool value)
```

## Examples


Shows how to lock style.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> styleHeading1 = doc->get_Styles()->idx_get(StyleIdentifier::Heading1);
if (!styleHeading1->get_Locked())
{
    styleHeading1->set_Locked(true);
}

doc->Save(get_ArtifactsDir() + u"Styles.LockStyle.docx");
```
## See Also

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

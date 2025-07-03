---
title: Aspose::Words::Style::get_Locked method
linktitle: get_Locked
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Style::get_Locked method. Specifies whether this style is locked in C++.'
type: docs
weight: 13500
url: /cpp/aspose.words/style/get_locked/
---
## Style::get_Locked method


Specifies whether this style is locked.

```cpp
bool Aspose::Words::Style::get_Locked() const
```


## Examples



Shows how to lock style. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> styleHeading1 = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1);
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

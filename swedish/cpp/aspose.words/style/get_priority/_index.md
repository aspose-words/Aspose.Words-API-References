---
title: "Aspose::Words::Style::get_Priority metod"
linktitle: "get_Priority"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Style::get_Priority metod. Hämtar/anger det heltal som representerar prioriteten för sortering av stilar i Stilar-uppgiftspanelen i C++."
type: docs
weight: 16334
url: /sv/cpp/aspose.words/style/get_priority/
---
## Style::get_Priority method


Hämtar/anger det heltal som representerar prioriteten för sortering av stilar i Stilpanelen.

```cpp
int32_t Aspose::Words::Style::get_Priority() const
```


## Exempel



Visar hur man prioriterar och döljer en stil.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> styleTitle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Subtitle);

if (styleTitle->get_Priority() == 9)
{
    styleTitle->set_Priority(10);
}

if (!styleTitle->get_UnhideWhenUsed())
{
    styleTitle->set_UnhideWhenUsed(true);
}

if (styleTitle->get_SemiHidden())
{
    styleTitle->set_SemiHidden(true);
}

doc->Save(get_ArtifactsDir() + u"Styles.StylePriority.docx");
```

## Se även

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

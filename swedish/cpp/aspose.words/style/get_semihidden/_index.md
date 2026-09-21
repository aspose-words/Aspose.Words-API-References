---
title: "Aspose::Words::Style::get_SemiHidden metod"
linktitle: "get_SemiHidden"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Style::get_SemiHidden metod. Hämtar/anger om stilen är dold i Stilar-galleriet och i Stilar-uppgiftspanelen i C++."
type: docs
weight: 16667
url: /sv/cpp/aspose.words/style/get_semihidden/
---
## Style::get_SemiHidden method


Hämtar/anger om stilen är dold i Stilgalleriet och i Stilpanelen.

```cpp
bool Aspose::Words::Style::get_SemiHidden() const
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

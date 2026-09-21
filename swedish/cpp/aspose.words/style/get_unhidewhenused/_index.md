---
title: "Aspose::Words::Style::get_UnhideWhenUsed metod"
linktitle: "get_UnhideWhenUsed"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Style::get_UnhideWhenUsed metod. Hämtar/sätter om stilen som används i det aktuella dokumentet avdöljs från Stilar-galleriet och från Stilar-uppgiftspanelen. Sant när den använda stilen ska visas i Stilar-galleriet i C++."
type: docs
weight: 19500
url: /sv/cpp/aspose.words/style/get_unhidewhenused/
---
## Style::get_UnhideWhenUsed method


Hämtar/anger om stilen som används i det aktuella dokumentet visas igen i Stilgalleriet och i Stilpanelen. Sant när den använda stilen ska visas i Stilgalleriet.

```cpp
bool Aspose::Words::Style::get_UnhideWhenUsed() const
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

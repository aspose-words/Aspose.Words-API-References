---
title: "Aspose::Words::Style::get_Priority Methode"
linktitle: "get_Priority"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Style::get_Priority Methode. Liest/legt den ganzzahligen Wert fest, der die Priorität für die Sortierung der Stile im Aufgabenbereich Stile in C++ darstellt."
type: docs
weight: 16334
url: /de/cpp/aspose.words/style/get_priority/
---
## Style::get_Priority method


Liest/Setzt den ganzzahligen Wert, der die Priorität für die Sortierung der Stile im Aufgabenbereich Stile darstellt.

```cpp
int32_t Aspose::Words::Style::get_Priority() const
```


## Beispiele



Zeigt, wie man einen Stil priorisiert und ausblendet.
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

## Siehe auch

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

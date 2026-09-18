---
title: "Aspose::Words::Style::get_UnhideWhenUsed Methode"
linktitle: "get_UnhideWhenUsed"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Style::get_UnhideWhenUsed Methode. Ruft ab/legt fest, ob der im aktuellen Dokument verwendete Stil aus der Stile‑Galerie und dem Stile‑Taskfeld wieder eingeblendet wird. True, wenn der verwendete Stil in der Stile‑Galerie in C++ angezeigt werden soll."
type: docs
weight: 19500
url: /de/cpp/aspose.words/style/get_unhidewhenused/
---
## Style::get_UnhideWhenUsed method


Liest/Setzt, ob der im aktuellen Dokument verwendete Stil in der Stile-Galerie und im Aufgabenbereich Stile wieder eingeblendet wird. Wahr, wenn der verwendete Stil in der Stile-Galerie angezeigt werden soll.

```cpp
bool Aspose::Words::Style::get_UnhideWhenUsed() const
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

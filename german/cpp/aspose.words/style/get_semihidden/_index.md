---
title: "Aspose::Words::Style::get_SemiHidden-Methode"
linktitle: "get_SemiHidden"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Style::get_SemiHidden-Methode. Gibt an/legt fest, ob der Stil in der Stilgalerie und im Stil‑Task‑Paneel in C++ ausgeblendet wird."
type: docs
weight: 16667
url: /de/cpp/aspose.words/style/get_semihidden/
---
## Style::get_SemiHidden method


Liest/Setzt, ob der Stil in der Stile-Galerie und im Aufgabenbereich Stile ausgeblendet wird.

```cpp
bool Aspose::Words::Style::get_SemiHidden() const
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

---
title: "Aspose::Words::Style::get_Priority metodo"
linktitle: "get_Priority"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Style::get_Priority metodo. Ottiene/imposta il valore intero che rappresenta la priorità per ordinare gli stili nel riquadro attività Stili in C++."
type: docs
weight: 16334
url: /it/cpp/aspose.words/style/get_priority/
---
## Style::get_Priority method


Ottiene/Imposta il valore intero che rappresenta la priorità per l'ordinamento degli stili nel riquadro attività Stili.

```cpp
int32_t Aspose::Words::Style::get_Priority() const
```


## Esempi



Mostra come dare priorità e nascondere uno stile.
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

## Vedi anche

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

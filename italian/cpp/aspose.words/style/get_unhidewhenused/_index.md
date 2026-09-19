---
title: "Metodo Aspose::Words::Style::get_UnhideWhenUsed"
linktitle: "get_UnhideWhenUsed"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Style::get_UnhideWhenUsed. Ottiene/imposta se lo stile utilizzato nel documento corrente viene mostrato nella galleria Stili e nel riquadro attività Stili. True quando lo stile usato deve essere mostrato nella galleria Stili in C++."
type: docs
weight: 19500
url: /it/cpp/aspose.words/style/get_unhidewhenused/
---
## Style::get_UnhideWhenUsed method


Ottiene/imposta se lo stile utilizzato nel documento corrente viene mostrato nella galleria Stili e nel riquadro attività Stili. True quando lo stile usato deve essere visualizzato nella galleria Stili.

```cpp
bool Aspose::Words::Style::get_UnhideWhenUsed() const
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

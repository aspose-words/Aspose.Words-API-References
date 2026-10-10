---
title: "Énumération Aspose::Words::BaselineAlignment"
linktitle: "BaselineAlignment"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Énumération Aspose::Words::BaselineAlignment. Spécifie la position verticale des polices sur une ligne en C++."
type: docs
weight: 80500
url: /fr/cpp/aspose.words/baselinealignment/
---
## BaselineAlignment enum


Spécifie la position verticale des polices sur une ligne.

```cpp
enum class BaselineAlignment
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Top | 0 | Aligne le haut de chaque police. |
| Centre | 1 | Aligne les points centraux de chaque police. |
| Baseline | 2 | Aligne à la ligne de base du paragraphe. |
| Bottom | 3 | Aligne le bas de chaque police. |
| Auto | 4 | La ligne de base est ajustée automatiquement. |


## Exemples



Montre comment définir la position verticale des polices sur une ligne.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();
if (format->get_BaselineAlignment() == Aspose::Words::BaselineAlignment::Auto)
{
    format->set_BaselineAlignment(Aspose::Words::BaselineAlignment::Top);
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphBaselineAlignment.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

---
title: "Aspose::Words::Loading::LoadOptions::get_MswVersion method"
linktitle: "get_MswVersion"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::LoadOptions::get_MswVersion method. Permet de spécifier que le processus de chargement du document doit correspondre à une version spécifique de MS Word. La valeur par défaut est Word2019 en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.loading/loadoptions/get_mswversion/
---
## LoadOptions::get_MswVersion method


Permet de spécifier que le processus de chargement du document doit correspondre à une version spécifique de MS Word. La valeur par défaut est [Word2019](../../../aspose.words.settings/mswordversion/)

```cpp
Aspose::Words::Settings::MsWordVersion Aspose::Words::Loading::LoadOptions::get_MswVersion() const
```


## Exemples



Montre comment émuler la procédure de chargement d'une version spécifique de Microsoft Word lors du chargement du document.
```cpp
// Par défaut, Aspose.Words charge les documents selon la spécification Microsoft Word 2019.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

ASSERT_EQ(Aspose::Words::Settings::MsWordVersion::Word2019, loadOptions->get_MswVersion());

// Ce document ne possède pas le style de mise en forme de paragraphe par défaut.
// Ce style par défaut sera régénéré lorsque nous chargerons le document avec Microsoft Word ou Aspose.Words.
loadOptions->set_MswVersion(Aspose::Words::Settings::MsWordVersion::Word2007);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

// L'interligne du style aura cette valeur lorsqu'il est chargé selon la spécification Microsoft Word 2007.
ASSERT_NEAR(12.95, doc->get_Styles()->get_DefaultParagraphFormat()->get_LineSpacing(), 0.01);
```

## Voir aussi

* Enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)

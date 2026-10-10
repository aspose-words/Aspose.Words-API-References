---
title: "Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing méthode"
linktitle: "get_AdjustSentenceAndWordSpacing"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing méthode. Obtient ou définit une valeur booléenne qui indique si l'espacement des phrases et des mots doit être ajusté automatiquement. La valeur par défaut est false en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/importformatoptions/get_adjustsentenceandwordspacing/
---
## ImportFormatOptions::get_AdjustSentenceAndWordSpacing method


Obtient ou définit une valeur booléenne qui indique s'il faut ajuster automatiquement l'espacement des phrases et des mots. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing() const
```


## Exemples



Montre comment ajuster automatiquement l'espacement des phrases et des mots.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);
builder->Write(u"Dolor sit amet.");

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->Write(u"Lorem ipsum.");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AdjustSentenceAndWordSpacing(true);
builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, options);

ASSERT_EQ(u"Lorem ipsum. Dolor sit amet.", dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```

## Voir aussi

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

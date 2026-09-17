---
title: "Méthode Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage"
linktitle: "get_AppendDocumentWithNewPage"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage. Obtient ou définit une valeur booléenne indiquant s'il faut changer le type de la première section importée en NewPage de manière forcée lors de l'appel à AppendDocument(). La valeur par défaut est true en C++."
type: docs
weight: 3500
url: /fr/cpp/aspose.words/importformatoptions/get_appenddocumentwithnewpage/
---
## ImportFormatOptions::get_AppendDocumentWithNewPage method


Obtient ou définit une valeur booléenne indiquant s'il faut changer le type de la première section importée en [NewPage](../../sectionstart/) de manière forcée lors de l'appel à [AppendDocument()](../). La valeur par défaut est **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage() const
```


## Exemples



Montre comment préserver le type de section original.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::Continuous);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AppendDocumentWithNewPage(false);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

ASSERT_EQ(Aspose::Words::SectionStart::Continuous, dstDoc->get_Sections()->idx_get(1)->get_PageSetup()->get_SectionStart());
```

## Voir aussi

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

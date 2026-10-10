---
title: "Aspose::Words::Document::get_HyphenationOptions method"
linktitle: "get_HyphenationOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_HyphenationOptions method. Fournit l'accès aux options de césure du document en C++."
type: docs
weight: 32000
url: /fr/cpp/aspose.words/document/get_hyphenationoptions/
---
## Document::get_HyphenationOptions method


Fournit l'accès aux options de césure du document.

```cpp
System::SharedPtr<Aspose::Words::Settings::HyphenationOptions> Aspose::Words::Document::get_HyphenationOptions()
```


## Exemples



Montre comment configurer la césure automatique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(24);
builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->get_HyphenationOptions()->set_AutoHyphenation(true);
doc->get_HyphenationOptions()->set_ConsecutiveHyphenLimit(2);
doc->get_HyphenationOptions()->set_HyphenationZone(720);
doc->get_HyphenationOptions()->set_HyphenateCaps(true);

doc->Save(get_ArtifactsDir() + u"Document.HyphenationOptions.docx");
```

## Voir aussi

* Class [HyphenationOptions](../../../aspose.words.settings/hyphenationoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

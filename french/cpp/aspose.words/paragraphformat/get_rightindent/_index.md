---
title: "Aspose::Words::ParagraphFormat::get_RightIndent méthode"
linktitle: "get_RightIndent"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ParagraphFormat::get_RightIndent méthode. Obtient ou définit la valeur (en points) qui représente le retrait droit du paragraphe en C++."
type: docs
weight: 28000
url: /fr/cpp/aspose.words/paragraphformat/get_rightindent/
---
## ParagraphFormat::get_RightIndent method


Obtient ou définit la valeur (en points) qui représente le retrait droit du paragraphe.

```cpp
double Aspose::Words::ParagraphFormat::get_RightIndent()
```


## Exemples



Montre comment configurer le formatage de paragraphe pour créer du texte décentré.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Centrer tout le texte que le générateur de documents écrit, et configurer les retraits.
// La configuration de retrait ci-dessous créera un bloc de texte qui sera placé de manière asymétrique sur la page.
// Le "centre" auquel nous alignons le texte sera le milieu du corps du texte, pas le milieu de la page.
System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
paragraphFormat->set_LeftIndent(100);
paragraphFormat->set_RightIndent(50);
paragraphFormat->set_SpaceAfter(25);

builder->Writeln(u"This paragraph demonstrates how left and right indentation affects word wrapping.");
builder->Writeln(u"The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetParagraphFormatting.docx");
```

## Voir aussi

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Aspose::Words::Paragraph::get_IsEndOfDocument méthode"
linktitle: "get_IsEndOfDocument"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Paragraph::get_IsEndOfDocument méthode. Vrai si ce paragraphe est le dernier paragraphe de la dernière section du document en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words/paragraph/get_isendofdocument/
---
## Paragraph::get_IsEndOfDocument method


Vrai si ce paragraphe est le dernier paragraphe de la dernière section du document.

```cpp
bool Aspose::Words::Paragraph::get_IsEndOfDocument()
```


## Exemples



Montre comment insérer un paragraphe dans le document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Arial");
font->set_Underline(Aspose::Words::Underline::Dash);

System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_FirstLineIndent(8);
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Justify);
paragraphFormat->set_AddSpaceBetweenFarEastAndAlpha(true);
paragraphFormat->set_AddSpaceBetweenFarEastAndDigit(true);
paragraphFormat->set_KeepTogether(true);

// La méthode "Writeln" termine le paragraphe après avoir ajouté du texte
// et commence ensuite une nouvelle ligne, ajoutant un nouveau paragraphe.
builder->Writeln(u"Hello world!");

ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsEndOfDocument());
```

## Voir aussi

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

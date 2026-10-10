---
title: "Méthode Aspose::Words::ParagraphFormat::get_FirstLineIndent"
linktitle: "get_FirstLineIndent"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::ParagraphFormat::get_FirstLineIndent. Obtient ou définit la valeur (en points) d'un retrait de première ligne ou suspendu. Utilisez des valeurs positives pour définir le retrait de première ligne, et des valeurs négatives pour définir le retrait suspendu en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words/paragraphformat/get_firstlineindent/
---
## ParagraphFormat::get_FirstLineIndent method


Obtient ou définit la valeur (en points) pour un retrait de première ligne ou un retrait suspendu. Utilisez des valeurs positives pour définir le retrait de première ligne, et des valeurs négatives pour définir le retrait suspendu.

```cpp
double Aspose::Words::ParagraphFormat::get_FirstLineIndent()
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

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

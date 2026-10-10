---
title: "Méthode Aspose::Words::Font::get_TintAndShade"
linktitle: "get_TintAndShade"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::get_TintAndShade. Obtient ou définit une valeur double qui éclaircit ou assombrit une couleur en C++."
type: docs
weight: 54000
url: /fr/cpp/aspose.words/font/get_tintandshade/
---
## Font::get_TintAndShade method


Obtient ou définit une valeur double qui éclaircit ou assombrit une couleur.

```cpp
double Aspose::Words::Font::get_TintAndShade()
```

## Remarques


Les valeurs autorisées sont comprises entre -1 (le plus sombre) et 1 (le plus clair) pour cette propriété.

Zéro (0) est neutre.

## Exemples



Montre comment créer et utiliser un style thématisé.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Créez un style avec les propriétés de police du thème.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"ThemedStyle");
style->get_Font()->set_ThemeFont(Aspose::Words::Themes::ThemeFont::Major);
style->get_Font()->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent5);
style->get_Font()->set_TintAndShade(0.3);

builder->get_ParagraphFormat()->set_StyleName(u"ThemedStyle");
builder->Writeln(u"Text with themed style");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Aspose::Words::Font classe"
linktitle: "Police"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font classe. Contient les attributs de police (nom de police, taille de police, couleur, etc.) pour un objet. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 29000
url: /fr/cpp/aspose.words/font/
---
## Font class


Contient les attributs de police (nom de police, taille de police, couleur, etc.) pour un objet. Pour en savoir plus, consultez l'article de documentation [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class Font : public Aspose::Words::IBorderAttrSource,
             public Aspose::Words::IShadingAttrSource,
             public Aspose::Words::Drawing::Core::IFillable
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Réinitialise le formatage de police par défaut. |
| [get_AllCaps](./get_allcaps/)() | Vrai si la police est formatée en majuscules. |
| [get_AutoColor](./get_autocolor/)() | Renvoie la couleur calculée actuelle du texte (noir ou blanc) à utiliser pour 'auto color'. Si la couleur n'est pas 'auto', renvoie alors [Color](./get_color/). |
| [get_Bidi](./get_bidi/)() | Spécifie si le contenu de cet enchaînement doit avoir des caractéristiques de droite à gauche. |
| [get_Bold](./get_bold/)() | Vrai si la police est formatée en gras. |
| [get_BoldBi](./get_boldbi/)() | Vrai si le texte de droite à gauche est formaté en gras. |
| [get_Border](./get_border/)() | Renvoie un objet [Border](../border/) qui spécifie la bordure pour la police. |
| [get_Color](./get_color/)() | Obtient ou définit la couleur de la police. |
| [get_ComplexScript](./get_complexscript/)() | Spécifie si le contenu de cet enchaînement doit être traité comme du texte à script complexe, indépendamment de leurs valeurs de caractères Unicode, lors de la détermination du formatage de cet enchaînement. |
| [get_DoubleStrikeThrough](./get_doublestrikethrough/)() | Vrai si la police est formatée avec un double barré. |
| [get_Emboss](./get_emboss/)() | Vrai si la police est formatée en relief. |
| [get_EmphasisMark](./get_emphasismark/)() | Obtient ou définit le signe d'emphase appliqué à ce formatage. |
| [get_Engrave](./get_engrave/)() | Vrai si la police est formatée en gravure. |
| [get_Fill](./get_fill/)() | Obtient le format de remplissage pour la [Font](./). |
| [get_Hidden](./get_hidden/)() | Vrai si la police est formatée comme texte masqué. |
| [get_HighlightColor](./get_highlightcolor/)() | Obtient ou définit la couleur de surbrillance (marqueur). |
| [get_Italic](./get_italic/)() | Vrai si la police est formatée en italique. |
| [get_ItalicBi](./get_italicbi/)() | Vrai si le texte de droite à gauche est formaté en italique. |
| [get_Kerning](./get_kerning/)() | Obtient ou définit la taille de police à laquelle le crénage commence. |
| [get_LineSpacing](./get_linespacing/)() | Renvoie l'interligne de cette police (en points). |
| [get_LocaleId](./get_localeid/)() | Obtient ou définit l'identifiant de paramètre régional (langue) des caractères formatés. |
| [get_LocaleIdBi](./get_localeidbi/)() | Obtient ou définit l'identifiant de paramètre régional (langue) des caractères formatés de droite à gauche. |
| [get_LocaleIdFarEast](./get_localeidfareast/)() | Obtient ou définit l'identifiant de paramètre régional (langue) des caractères asiatiques formatés. |
| [get_Name](./get_name/)() | Obtient ou définit le nom de la police. |
| [get_NameAscii](./get_nameascii/)() | Renvoie ou définit la police utilisée pour le texte latin (caractères avec des codes de caractères de 0 (zéro) à 127). |
| [get_NameBi](./get_namebi/)() | Renvoie ou définit le nom de la police dans un document de langue de droite à gauche. |
| [get_NameFarEast](./get_namefareast/)() | Renvoie ou définit un nom de police d'Asie de l'Est. |
| [get_NameOther](./get_nameother/)() | Renvoie ou définit la police utilisée pour les caractères dont les codes sont compris entre 128 et 255. |
| [get_NoProofing](./get_noproofing/)() | Vrai lorsque les caractères formatés ne doivent pas être vérifiés orthographiquement. |
| [get_NumberSpacing](./get_numberspacing/)() | Obtient ou définit le type d'espacement du chiffre affiché. |
| [get_Outline](./get_outline/)() | Vrai si la police est formatée en contour. |
| [get_Position](./get_position/)() | Obtient ou définit la position du texte (en points) par rapport à la ligne de base. Un nombre positif élève le texte, et un nombre négatif l'abaisse. |
| [get_Scaling](./get_scaling/)() | Obtient ou définit le redimensionnement de la largeur des caractères en pourcentage. |
| [get_Shading](./get_shading/)() | Renvoie un objet [Shading](../shading/) qui fait référence au format d’ombrage de la police. |
| [get_Shadow](./get_shadow/)() | Vrai si la police est formatée avec une ombre. |
| [get_Size](./get_size/)() | Obtient ou définit la taille de la police en points. |
| [get_SizeBi](./get_sizebi/)() | Obtient ou définit la taille de la police en points utilisée dans un document de droite à gauche. |
| [get_SmallCaps](./get_smallcaps/)() | Vrai si la police est formatée en petites majuscules. |
| [get_SnapToGrid](./get_snaptogrid/)() | Spécifie si la police actuelle doit utiliser les paramètres de caractères par ligne de la grille du document lors de la mise en page. |
| [get_Spacing](./get_spacing/)() | Renvoie ou définit l'espacement (en points) entre les caractères. |
| [get_StrikeThrough](./get_strikethrough/)() | Vrai si la police est formatée avec du texte barré. |
| [get_Style](./get_style/)() | Obtient ou définit le style de caractère appliqué à ce formatage. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Obtient ou définit l'identifiant de style indépendant de la locale du style de caractère appliqué à ce formatage. |
| [get_StyleName](./get_stylename/)() | Obtient ou définit le nom du style de caractère appliqué à ce formatage. |
| [get_Subscript](./get_subscript/)() | Vrai si la police est formatée en indice. |
| [get_Superscript](./get_superscript/)() | Vrai si la police est formatée en exposant. |
| [get_TextEffect](./get_texteffect/)() | Obtient ou définit l'effet d'animation de la police. |
| [get_ThemeColor](./get_themecolor/)() | Obtient ou définit la couleur du thème dans le schéma de couleurs appliqué associé à cet objet [Font](./). |
| [get_ThemeFont](./get_themefont/)() | Obtient ou définit la police du thème dans le schéma de polices appliqué associé à cet objet [Font](./). |
| [get_ThemeFontAscii](./get_themefontascii/)() | Obtient ou définit la police du thème utilisée pour le texte latin (caractères dont les codes vont de 0 (zéro) à 127) dans le schéma de polices appliqué associé à cet objet [Font](./). |
| [get_ThemeFontBi](./get_themefontbi/)() | Obtient ou définit la police du thème dans le schéma de polices appliqué associé à cet objet [Font](./) dans un document de langue de droite à gauche. |
| [get_ThemeFontFarEast](./get_themefontfareast/)() | Obtient ou définit la police du thème est-asiatique dans le schéma de polices appliqué associé à cet objet [Font](./). |
| [get_ThemeFontOther](./get_themefontother/)() | Obtient ou définit la police de thème utilisée pour les caractères dont les codes sont compris entre 128 et 255 dans le schéma de police appliqué qui est associé à cet objet [Font](./). |
| [get_TintAndShade](./get_tintandshade/)() | Obtient ou définit une valeur double qui éclaircit ou assombrit une couleur. |
| [get_Underline](./get_underline/)() | Obtient ou définit le type de soulignement appliqué à la police. |
| [get_UnderlineColor](./get_underlinecolor/)() | Obtient ou définit la couleur du soulignement appliqué à la police. |
| [GetType](./gettype/)() const override |  |
| [HasDmlEffect](./hasdmleffect/)(Aspose::Words::TextDmlEffect) | Vérifie si un effet de texte DrawingML particulier est appliqué. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllCaps](./set_allcaps/)(bool) | Définisseur pour [Aspose::Words::Font::get_AllCaps](./get_allcaps/). |
| [set_Bidi](./set_bidi/)(bool) | Définisseur pour [Aspose::Words::Font::get_Bidi](./get_bidi/). |
| [set_Bold](./set_bold/)(bool) | Définisseur pour [Aspose::Words::Font::get_Bold](./get_bold/). |
| [set_BoldBi](./set_boldbi/)(bool) | Définisseur pour [Aspose::Words::Font::get_BoldBi](./get_boldbi/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Définisseur pour [Aspose::Words::Font::get_Color](./get_color/). |
| [set_ComplexScript](./set_complexscript/)(bool) | Définisseur pour [Aspose::Words::Font::get_ComplexScript](./get_complexscript/). |
| [set_DoubleStrikeThrough](./set_doublestrikethrough/)(bool) | Définisseur pour [Aspose::Words::Font::get_DoubleStrikeThrough](./get_doublestrikethrough/). |
| [set_Emboss](./set_emboss/)(bool) | Définisseur pour [Aspose::Words::Font::get_Emboss](./get_emboss/). |
| [set_EmphasisMark](./set_emphasismark/)(Aspose::Words::EmphasisMark) | Définisseur pour [Aspose::Words::Font::get_EmphasisMark](./get_emphasismark/). |
| [set_Engrave](./set_engrave/)(bool) | Définisseur pour [Aspose::Words::Font::get_Engrave](./get_engrave/). |
| [set_Hidden](./set_hidden/)(bool) | Définisseur pour [Aspose::Words::Font::get_Hidden](./get_hidden/). |
| [set_HighlightColor](./set_highlightcolor/)(System::Drawing::Color) | Définisseur pour [Aspose::Words::Font::get_HighlightColor](./get_highlightcolor/). |
| [set_Italic](./set_italic/)(bool) | Définisseur pour [Aspose::Words::Font::get_Italic](./get_italic/). |
| [set_ItalicBi](./set_italicbi/)(bool) | Définisseur pour [Aspose::Words::Font::get_ItalicBi](./get_italicbi/). |
| [set_Kerning](./set_kerning/)(double) | Définisseur pour [Aspose::Words::Font::get_Kerning](./get_kerning/). |
| [set_LocaleId](./set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Font::get_LocaleId](./get_localeid/). |
| [set_LocaleIdBi](./set_localeidbi/)(int32_t) | Définisseur pour [Aspose::Words::Font::get_LocaleIdBi](./get_localeidbi/). |
| [set_LocaleIdFarEast](./set_localeidfareast/)(int32_t) | Définisseur pour [Aspose::Words::Font::get_LocaleIdFarEast](./get_localeidfareast/). |
| [set_Name](./set_name/)(const System::String\&) | Définisseur pour [Aspose::Words::Font::get_Name](./get_name/). |
| [set_NameAscii](./set_nameascii/)(const System::String\&) | Définisseur pour [Aspose::Words::Font::get_NameAscii](./get_nameascii/). |
| [set_NameBi](./set_namebi/)(const System::String\&) | Définisseur pour [Aspose::Words::Font::get_NameBi](./get_namebi/). |
| [set_NameFarEast](./set_namefareast/)(const System::String\&) | Définisseur de [Aspose::Words::Font::get_NameFarEast](./get_namefareast/). |
| [set_NameOther](./set_nameother/)(const System::String\&) | Définisseur de [Aspose::Words::Font::get_NameOther](./get_nameother/). |
| [set_NoProofing](./set_noproofing/)(bool) | Définisseur de [Aspose::Words::Font::get_NoProofing](./get_noproofing/). |
| [set_NumberSpacing](./set_numberspacing/)(Aspose::Words::NumSpacing) | Définisseur de [Aspose::Words::Font::get_NumberSpacing](./get_numberspacing/). |
| [set_Outline](./set_outline/)(bool) | Définisseur de [Aspose::Words::Font::get_Outline](./get_outline/). |
| [set_Position](./set_position/)(double) | Définisseur de [Aspose::Words::Font::get_Position](./get_position/). |
| [set_Scaling](./set_scaling/)(int32_t) | Définisseur de [Aspose::Words::Font::get_Scaling](./get_scaling/). |
| [set_Shadow](./set_shadow/)(bool) | Définisseur de [Aspose::Words::Font::get_Shadow](./get_shadow/). |
| [set_Size](./set_size/)(double) | Définisseur de [Aspose::Words::Font::get_Size](./get_size/). |
| [set_SizeBi](./set_sizebi/)(double) | Définisseur de [Aspose::Words::Font::get_SizeBi](./get_sizebi/). |
| [set_SmallCaps](./set_smallcaps/)(bool) | Définisseur de [Aspose::Words::Font::get_SmallCaps](./get_smallcaps/). |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | Spécifie si la police actuelle doit utiliser les paramètres de caractères par ligne de la grille du document lors de la mise en page. |
| [set_Spacing](./set_spacing/)(double) | Définisseur de [Aspose::Words::Font::get_Spacing](./get_spacing/). |
| [set_StrikeThrough](./set_strikethrough/)(bool) | Définisseur de [Aspose::Words::Font::get_StrikeThrough](./get_strikethrough/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Définisseur de [Aspose::Words::Font::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Définisseur de [Aspose::Words::Font::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Définisseur de [Aspose::Words::Font::get_StyleName](./get_stylename/). |
| [set_Subscript](./set_subscript/)(bool) | Définisseur de [Aspose::Words::Font::get_Subscript](./get_subscript/). |
| [set_Superscript](./set_superscript/)(bool) | Définisseur de [Aspose::Words::Font::get_Superscript](./get_superscript/). |
| [set_TextEffect](./set_texteffect/)(Aspose::Words::TextEffect) | Définisseur de [Aspose::Words::Font::get_TextEffect](./get_texteffect/). |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | Définisseur de [Aspose::Words::Font::get_ThemeColor](./get_themecolor/). |
| [set_ThemeFont](./set_themefont/)(Aspose::Words::Themes::ThemeFont) | Définisseur de [Aspose::Words::Font::get_ThemeFont](./get_themefont/). |
| [set_ThemeFontAscii](./set_themefontascii/)(Aspose::Words::Themes::ThemeFont) | Définisseur de [Aspose::Words::Font::get_ThemeFontAscii](./get_themefontascii/). |
| [set_ThemeFontBi](./set_themefontbi/)(Aspose::Words::Themes::ThemeFont) | Définisseur de [Aspose::Words::Font::get_ThemeFontBi](./get_themefontbi/). |
| [set_ThemeFontFarEast](./set_themefontfareast/)(Aspose::Words::Themes::ThemeFont) | Définisseur de [Aspose::Words::Font::get_ThemeFontFarEast](./get_themefontfareast/). |
| [set_ThemeFontOther](./set_themefontother/)(Aspose::Words::Themes::ThemeFont) | Définisseur de [Aspose::Words::Font::get_ThemeFontOther](./get_themefontother/). |
| [set_TintAndShade](./set_tintandshade/)(double) | Définisseur pour [Aspose::Words::Font::get_TintAndShade](./get_tintandshade/). |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | Définisseur pour [Aspose::Words::Font::get_Underline](./get_underline/). |
| [set_UnderlineColor](./set_underlinecolor/)(System::Drawing::Color) | Définisseur pour [Aspose::Words::Font::get_UnderlineColor](./get_underlinecolor/). |
| static [Type](./type/)() |  |
## Remarques


Vous ne créez pas d'instances de la classe [Font](./) directement. Vous utilisez simplement [Font](./) pour accéder aux propriétés de police des différents objets tels que [Run](../run/), [Paragraph](../paragraph/), [Style](../style/), [DocumentBuilder](../documentbuilder/).

## Exemples



Montre comment insérer une chaîne entourée d'une bordure dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


Montre comment formater une séquence de texte en utilisant sa propriété de police.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```


Montre comment créer et utiliser un style de paragraphe avec un formatage de liste.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un style de paragraphe personnalisé.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Créez une liste et assurez-vous que les paragraphes qui utilisent ce style utiliseront cette liste.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Appliquez le style de paragraphe au paragraphe actuel du constructeur de document, puis ajoutez du texte.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Modifiez le style du DocumentBuilder pour qu'il n'ait aucun format de liste et écrivez un autre paragraphe.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

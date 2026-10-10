---
title: "Aspose::Words::Fonts::FontInfo classe"
linktitle: "FontInfo"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontInfo classe. Spécifie les informations sur une police utilisée dans le document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.fonts/fontinfo/
---
## FontInfo class


Spécifie les informations sur une police utilisée dans le document. Pour en savoir plus, visitez l’article de documentation [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontInfo : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_AltName](./get_altname/)() const | Obtient ou définit le nom alternatif de la police. |
| [get_Charset](./get_charset/)() | Obtient ou définit le jeu de caractères de la police. |
| [get_EmbeddingLicensingRights](./get_embeddinglicensingrights/)() | Obtient les droits de licence de la police incorporée. |
| [get_Family](./get_family/)() const | Obtient ou définit la famille de police à laquelle cette police appartient. |
| [get_IsTrueType](./get_istruetype/)() const | Indique que cette police est une police TrueType ou OpenType par opposition à une police raster ou vectorielle. La valeur par défaut est **true**. |
| [get_Name](./get_name/)() const | Obtient le nom de la police. |
| [get_Panose](./get_panose/)() const | Obtient ou définit le numéro de classification de police PANOSE. |
| [get_Pitch](./get_pitch/)() const | Le pitch indique si la police est à chasse fixe, à espacement proportionnel, ou dépend d'un paramètre par défaut. |
| [GetEmbeddedFont](./getembeddedfont/)(Aspose::Words::Fonts::EmbeddedFontFormat, Aspose::Words::Fonts::EmbeddedFontStyle) | Obtient un fichier de police incorporé spécifique. |
| [GetEmbeddedFontAsOpenType](./getembeddedfontasopentype/)(Aspose::Words::Fonts::EmbeddedFontStyle) | Obtient un fichier de police incorporé au format OpenType. [Polices](../) au format OpenType incorporé sont convertis en OpenType. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AltName](./set_altname/)(const System::String\&) | Définisseur pour [Aspose::Words::Fonts::FontInfo::get_AltName](./get_altname/). |
| [set_Charset](./set_charset/)(int32_t) | Définisseur pour [Aspose::Words::Fonts::FontInfo::get_Charset](./get_charset/). |
| [set_Family](./set_family/)(Aspose::Words::Fonts::FontFamily) | Définisseur pour [Aspose::Words::Fonts::FontInfo::get_Family](./get_family/). |
| [set_IsTrueType](./set_istruetype/)(bool) | Définisseur pour [Aspose::Words::Fonts::FontInfo::get_IsTrueType](./get_istruetype/). |
| [set_Panose](./set_panose/)(const System::ArrayPtr\<uint8_t\>\&) | Définisseur pour [Aspose::Words::Fonts::FontInfo::get_Panose](./get_panose/). |
| [set_Pitch](./set_pitch/)(Aspose::Words::Fonts::FontPitch) | Définisseur pour [Aspose::Words::Fonts::FontInfo::get_Pitch](./get_pitch/). |
| static [Type](./type/)() |  |
## Remarques


Vous ne créez pas d'instances de cette classe directement. Utilisez la propriété [FontInfos](../../aspose.words/documentbase/get_fontinfos/) pour accéder à la collection de polices définies dans un document.

## Exemples



Montre comment imprimer les détails des polices présentes dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Imprime toutes les polices utilisées et non utilisées dans le document.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```

## Voir aussi

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)

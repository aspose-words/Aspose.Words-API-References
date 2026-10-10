---
title: "Aspose::Words::Loading::MarkdownLoadOptions class"
linktitle: "MarkdownLoadOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::MarkdownLoadOptions class. Permet de spécifier des options supplémentaires lors du chargement d'un document Markdown dans un objet Document en C++."
type: docs
weight: 5500
url: /fr/cpp/aspose.words.loading/markdownloadoptions/
---
## MarkdownLoadOptions class


Permet de spécifier des options supplémentaires lors du chargement d'un document [Markdown](../../aspose.words/loadformat/) dans un objet [Document](../../aspose.words/document/).

```cpp
class MarkdownLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Obtient ou définit la chaîne qui sera utilisée pour résoudre les URI relatives trouvées dans le document en URI absolues lorsque cela est nécessaire. Peut être **null** ou une chaîne vide. La valeur par défaut est **null**. |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Obtient ou définit s'il faut convertir les images de métafichier ([Wmf](../) ou [Emf](../)) au format image [Png](../). |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | Obtient ou définit s'il faut convertir les formes contenant EquationXML en objets Office [Math](../../aspose.words.math/). |
| [get_Encoding](../loadoptions/get_encoding/)() const | Obtient ou définit l'encodage qui sera utilisé pour charger un document HTML, TXT ou CHM si l'encodage n'est pas spécifié dans le document. Peut être **null**. La valeur par défaut est **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Permet de spécifier les paramètres de police du document. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | Spécifie s'il faut ignorer les données OLE. |
| [get_ImportUnderlineFormatting](./get_importunderlineformatting/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut reconnaître une séquence de deux caractères plus "++" comme formatage de texte souligné. La valeur par défaut est **false**. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Obtient les préférences de langue qui seront utilisées lors du chargement du document. |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Spécifie le format du document à charger. La valeur par défaut est [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Permet de spécifier que le processus de chargement du document doit correspondre à une version spécifique de MS Word. La valeur par défaut est [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](../loadoptions/get_password/)() const | Obtient ou définit le mot de passe pour ouvrir un document chiffré. Peut être **null** ou une chaîne vide. La valeur par défaut est **null**. |
| [get_PreserveEmptyLines](./get_preserveemptylines/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut conserver les lignes vides lors du chargement d'un document [Markdown](../../aspose.words/loadformat/). La valeur par défaut est **false**. Normalement, les lignes vides entre les éléments de niveau bloc dans Markdown sont ignorées. Les lignes vides au début et à la fin du document sont également ignorées. Cette option permet d'importer ces lignes vides. |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Obtient ou définit s'il faut conserver le champ INCLUDEPICTURE lors de la lecture des formats Microsoft Word. La valeur par défaut est **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Appelé pendant le chargement d'un document et accepte les données sur la progression du chargement. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | Définit comment le document doit être traité en cas d'erreurs lors du chargement. Utilisez cette propriété pour spécifier si le système doit tenter de récupérer le document ou suivre un autre comportement défini. La valeur par défaut est [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Permet de contrôler comment les ressources externes (images, feuilles de style) sont chargées lorsqu'un document est importé depuis HTML, MHTML. |
| [get_SoftLineBreakCharacter](./get_softlinebreakcharacter/)() const | Obtient ou définit une valeur de caractère représentant **soft line break**. La valeur par défaut est **SPACE (U+0020)**. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Permet d'utiliser des fichiers temporaires lors de la lecture du document. Par défaut, cette propriété est **null** et aucun fichier temporaire n'est utilisé. |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | Spécifie s'il faut mettre à jour les champs avec l'attribut **dirty**. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Obtient ou définit s'il faut utiliser la valeur LCID obtenue du registre Windows pour déterminer les marges par défaut de la mise en page. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Appelé pendant une opération de chargement, lorsqu'un problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Initialise une nouvelle instance de cette classe avec les valeurs par défaut. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | Un raccourci pour initialiser une nouvelle instance de cette classe avec le mot de passe spécifié afin de charger un document chiffré. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Un raccourci pour initialiser une nouvelle instance de cette classe avec les propriétés définies aux valeurs spécifiées. |
| [MarkdownLoadOptions](./markdownloadoptions/)() | Initialise une nouvelle instance de la classe [MarkdownLoadOptions](./). |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_ImportUnderlineFormatting](./set_importunderlineformatting/)(bool) | Définisseur pour [Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting](./get_importunderlineformatting/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreserveEmptyLines](./set_preserveemptylines/)(bool) | Définisseur pour [Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines](./get_preserveemptylines/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Appelé pendant le chargement d'un document et accepte les données sur la progression du chargement. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Permet de contrôler comment les ressources externes (images, feuilles de style) sont chargées lorsqu'un document est importé depuis HTML, MHTML. |
| [set_SoftLineBreakCharacter](./set_softlinebreakcharacter/)(char16_t) | Définisseur pour [Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter](./get_softlinebreakcharacter/). |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Appelé pendant une opération de chargement, lorsqu'un problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage. |
| static [Type](./type/)() |  |

## Exemples



Montre comment préserver les lignes vides lors du chargement d'un document.
```cpp
System::String mdText = System::String::Format(u"{0}Line1{1}{2}Line2{3}{4}", System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine());
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(mdText));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_PreserveEmptyLines(true);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"\rLine1\r\rLine2\r\f", doc->GetText());
}
```

## Voir aussi

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)

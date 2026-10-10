---
title: "Aspose::Words::Loading::ChmLoadOptions class"
linktitle: "ChmLoadOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::ChmLoadOptions class. Permet de spécifier des options supplémentaires lors du chargement d'un document CHM dans un objet Document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.loading/chmloadoptions/
---
## ChmLoadOptions class


Permet de spécifier des options supplémentaires lors du chargement d'un document CHM dans un objet [Document](../../aspose.words/document/). Pour en savoir plus, consultez l'article de documentation [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class ChmLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [ChmLoadOptions](./chmloadoptions/)() | Initialise une nouvelle instance de cette classe avec les valeurs par défaut. |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Obtient ou définit la chaîne qui sera utilisée pour résoudre les URI relatives trouvées dans le document en URI absolues lorsque cela est nécessaire. Peut être **null** ou une chaîne vide. La valeur par défaut est **null**. |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Obtient ou définit s'il faut convertir les images de métafichier ([Wmf](../) ou [Emf](../)) au format image [Png](../). |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | Obtient ou définit s'il faut convertir les formes contenant EquationXML en objets Office [Math](../../aspose.words.math/). |
| [get_Encoding](../loadoptions/get_encoding/)() const | Obtient ou définit l'encodage qui sera utilisé pour charger un document HTML, TXT ou CHM si l'encodage n'est pas spécifié dans le document. Peut être **null**. La valeur par défaut est **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Permet de spécifier les paramètres de police du document. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | Spécifie s'il faut ignorer les données OLE. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Obtient les préférences de langue qui seront utilisées lors du chargement du document. |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Spécifie le format du document à charger. La valeur par défaut est [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Permet de spécifier que le processus de chargement du document doit correspondre à une version spécifique de MS Word. La valeur par défaut est [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_OriginalFileName](./get_originalfilename/)() const | Le nom du fichier CHM. La valeur par défaut est **null**. |
| [get_Password](../loadoptions/get_password/)() const | Obtient ou définit le mot de passe pour ouvrir un document chiffré. Peut être **null** ou une chaîne vide. La valeur par défaut est **null**. |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Obtient ou définit s'il faut conserver le champ INCLUDEPICTURE lors de la lecture des formats Microsoft Word. La valeur par défaut est **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Appelé pendant le chargement d'un document et accepte les données sur la progression du chargement. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | Définit comment le document doit être traité en cas d'erreurs lors du chargement. Utilisez cette propriété pour spécifier si le système doit tenter de récupérer le document ou suivre un autre comportement défini. La valeur par défaut est [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Permet de contrôler comment les ressources externes (images, feuilles de style) sont chargées lorsqu'un document est importé depuis HTML, MHTML. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Permet d'utiliser des fichiers temporaires lors de la lecture du document. Par défaut, cette propriété est **null** et aucun fichier temporaire n'est utilisé. |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | Spécifie s'il faut mettre à jour les champs avec l'attribut **dirty**. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Obtient ou définit s'il faut utiliser la valeur LCID obtenue du registre Windows pour déterminer les marges par défaut de la mise en page. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Appelé pendant une opération de chargement, lorsqu'un problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Initialise une nouvelle instance de cette classe avec les valeurs par défaut. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | Un raccourci pour initialiser une nouvelle instance de cette classe avec le mot de passe spécifié afin de charger un document chiffré. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Un raccourci pour initialiser une nouvelle instance de cette classe avec les propriétés définies aux valeurs spécifiées. |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_OriginalFileName](./set_originalfilename/)(const System::String\&) | Définisseur pour [Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName](./get_originalfilename/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Appelé pendant le chargement d'un document et accepte les données sur la progression du chargement. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Permet de contrôler comment les ressources externes (images, feuilles de style) sont chargées lorsqu'un document est importé depuis HTML, MHTML. |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Définisseur pour [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Appelé pendant une opération de chargement, lorsqu'un problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage. |
| static [Type](./type/)() |  |

## Exemples



Montre comment résoudre les URL comme "ms-its:myfile.chm::/index.htm".
```cpp
// Notre document contient des URL comme "ms-its:amhelp.chm::....htm", mais il a un nom différent,
// Les liens de fichiers .so ne fonctionnent pas après les avoir enregistrés en HTML.
// Nous devons définir le nom de fichier d'origine dans 'ChmLoadOptions' pour éviter ce comportement.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::ChmLoadOptions>();
loadOptions->set_OriginalFileName(u"amhelp.chm");

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::IO::File::ReadAllBytes(get_MyDir() + u"Document with ms-its links.chm")), loadOptions);

doc->Save(get_ArtifactsDir() + u"ExChmLoadOptions.OriginalFileName.html");
```

## Voir aussi

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)

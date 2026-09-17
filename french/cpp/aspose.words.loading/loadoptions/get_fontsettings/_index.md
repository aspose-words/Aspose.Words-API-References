---
title: "Méthode Aspose::Words::Loading::LoadOptions::get_FontSettings"
linktitle: "get_FontSettings"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Loading::LoadOptions::get_FontSettings. Permet de spécifier les paramètres de police du document en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.loading/loadoptions/get_fontsettings/
---
## LoadOptions::get_FontSettings method


Permet de spécifier les paramètres de police du document.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Loading::LoadOptions::get_FontSettings() const
```

## Remarques


Lors du chargement de certains formats, Aspose.Words peut nécessiter de résoudre les polices. Par exemple, lors du chargement de documents HTML, [Aspose.Words](../../../aspose.words/) peut résoudre les polices pour effectuer un repli de police.

Si défini sur **null**, les paramètres de police statiques par défaut [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/) seront utilisés.

La valeur par défaut est **null**.

## Exemples



Montre comment désigner des substituts de police lors du chargement.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// Définissez une règle de substitution de police pour un objet LoadOptions.
// Si le document que nous chargeons utilise une police que nous ne possédons pas,
// cette règle remplacera la police indisponible par une police existante.
// Dans ce cas, toutes les utilisations de "MissingFont" seront converties en "Comic Sans MS".
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> substitutionRule = loadOptions->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution();
substitutionRule->AddSubstitutes(u"MissingFont", System::MakeArray<System::String>({u"Comic Sans MS"}));

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.html", loadOptions);

// À ce stade, ce texte sera toujours dans "MissingFont".
// La substitution de police aura lieu lorsque nous rendrons le document.
ASSERT_EQ(u"MissingFont", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());

doc->Save(get_ArtifactsDir() + u"FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```


Montre comment appliquer les paramètres de substitution de police lors du chargement d'un document.
```cpp
// Créez un objet FontSettings qui remplacera la police "Times New Roman"
// par la police "Arvo" provenant de notre dossier "MyFonts".
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->SetFontsFolder(get_FontsDir(), false);
fontSettings->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));

// Définissez cet objet FontSettings comme propriété d'un nouvel objet LoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_FontSettings(fontSettings);

// Chargez le document, puis rendez-le au format PDF avec la substitution de police.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.FontSettings.pdf");
```

## Voir aussi

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)

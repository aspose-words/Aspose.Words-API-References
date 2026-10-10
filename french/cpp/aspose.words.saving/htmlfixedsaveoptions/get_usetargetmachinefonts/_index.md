---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts méthode"
linktitle: "get_UseTargetMachineFonts"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts méthode. Le drapeau indique si les polices de la machine cible doivent être utilisées pour afficher le document. Si ce drapeau est défini sur true, les propriétés FontFormat et ExportEmbeddedFonts n'ont aucun effet, de plus ResourceSavingCallback n'est pas déclenché pour les polices. La valeur par défaut est false en C++."
type: docs
weight: 20000
url: /fr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_usetargetmachinefonts/
---
## HtmlFixedSaveOptions::get_UseTargetMachineFonts method


Le drapeau indique si les polices de la machine cible doivent être utilisées pour afficher le document. Si ce drapeau est défini sur **true**, les propriétés [FontFormat](../get_fontformat/) et [ExportEmbeddedFonts](../get_exportembeddedfonts/) n'ont aucun effet, de plus le [ResourceSavingCallback](../get_resourcesavingcallback/) n'est pas déclenché pour les polices. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts() const
```


## Exemples



Montre comment n'utiliser que les polices de la machine cible lors de l'enregistrement d'un document au format HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Bullet points with alternative font.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_ExportEmbeddedCss(true);
saveOptions->set_UseTargetMachineFonts(useTargetMachineFonts);
saveOptions->set_FontFormat(Aspose::Words::Saving::ExportFontFormat::Ttf);
saveOptions->set_ExportEmbeddedFonts(false);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UsingMachineFonts.html");

if (useTargetMachineFonts)
{
    ASSERT_FALSE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face")->get_Success());
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], ") + u"url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; }")->get_Success());
}
```

## Voir aussi

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

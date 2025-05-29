---
title: LoadOptions.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words pour .NET
description: Personnalisez les paramètres de police de vos documents avec LoadOptions FontSettings pour une lisibilité et un style améliorés. Optimisez vos documents sans effort !
type: docs
weight: 60
url: /fr/net/aspose.words.loading/loadoptions/fontsettings/
---
## LoadOptions.FontSettings property

Permet de spécifier les paramètres de police du document.

```csharp
public FontSettings FontSettings { get; set; }
```

## Remarques

Lors du chargement de certains formats, Aspose.Words peut nécessiter la résolution des polices. Par exemple, lors du chargement de documents HTML, Aspose.Words peut résoudre les polices pour effectuer une sauvegarde de polices.

Si défini sur`nul` , paramètres de police statique par défaut[`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) sera utilisé.

La valeur par défaut est`nul`.

## Exemples

Montre comment appliquer les paramètres de substitution de police lors du chargement d'un document.

```csharp
// Créez un objet FontSettings qui remplacera la police « Times New Roman »
// avec la police "Arvo" de notre dossier "MyFonts".
FontSettings fontSettings = new FontSettings();
fontSettings.SetFontsFolder(FontsDir, false);
fontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Times New Roman", "Arvo");

// Définissez cet objet FontSettings comme propriété d'un objet LoadOptions nouvellement créé.
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = fontSettings;

// Chargez le document, puis restituez-le au format PDF avec la substitution de police.
Document doc = new Document(MyDir + "Document.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.FontSettings.pdf");
```

Montre comment désigner des substituts de police pendant le chargement.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = new FontSettings();

// Définissez une règle de substitution de police pour un objet LoadOptions.
// Si le document que nous chargeons utilise une police que nous n'avons pas,
// cette règle remplacera la police indisponible par une police qui existe.
// Dans ce cas, toutes les utilisations de « MissingFont » seront converties en « Comic Sans MS ».
TableSubstitutionRule substitutionRule = loadOptions.FontSettings.SubstitutionSettings.TableSubstitution;
substitutionRule.AddSubstitutes("MissingFont", "Comic Sans MS");

Document doc = new Document(MyDir + "Missing font.html", loadOptions);

// À ce stade, ce texte sera toujours dans « MissingFont ».
// La substitution de police aura lieu lorsque nous rendrons le document.
Assert.AreEqual("MissingFont", doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Name);

doc.Save(ArtifactsDir + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```

### Voir également

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)

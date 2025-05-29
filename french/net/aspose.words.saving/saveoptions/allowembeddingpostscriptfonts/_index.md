---
title: SaveOptions.AllowEmbeddingPostScriptFonts
linktitle: AllowEmbeddingPostScriptFonts
articleTitle: AllowEmbeddingPostScriptFonts
second_title: Aspose.Words pour .NET
description: Contrôlez l'intégration des polices dans vos documents avec la fonction AllowEmbeddingPostScriptFonts de SaveOptions. Gérez facilement les options de polices TrueType pour une qualité de document améliorée.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/
---
## SaveOptions.AllowEmbeddingPostScriptFonts property

Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec des contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est`FAUX` .

```csharp
public bool AllowEmbeddingPostScriptFonts { get; set; }
```

## Remarques

Remarque : Word n’intègre pas les polices PostScript, mais peut ouvrir des documents avec des polices intégrées de ce type.

Cette option ne fonctionne que lorsque[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) du [`FontInfos`](../../../aspose.words/documentbase/fontinfos/) la propriété est définie sur`vrai`.

## Exemples

Montre comment enregistrer le document avec la police PostScript.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "PostScriptFont";
builder.Writeln("Some text with PostScript font.");

// Chargez la police avec PostScript à utiliser dans le document.
MemoryFontSource otf = new MemoryFontSource(File.ReadAllBytes(FontsDir + "AllegroOpen.otf"));
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] { otf });

// Intégrer les polices TrueType.
doc.FontInfos.EmbedTrueTypeFonts = true;

// Autoriser l'intégration de polices PostScript lors de l'intégration de polices TrueType.
// Microsoft Word n'intègre pas les polices PostScript, mais peut ouvrir des documents avec des polices intégrées de ce type.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Docx);
saveOptions.AllowEmbeddingPostScriptFonts = true;

doc.Save(ArtifactsDir + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)

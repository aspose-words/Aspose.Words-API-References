---
title: Font.LocaleIdFarEast
linktitle: LocaleIdFarEast
articleTitle: LocaleIdFarEast
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Font LocaleIdFarEast pour gérer facilement les identifiants régionaux des caractères asiatiques formatés, améliorant ainsi vos applications multilingues.
type: docs
weight: 220
url: /fr/net/aspose.words/font/localeidfareast/
---
## Font.LocaleIdFarEast property

Obtient ou définit l'identifiant régional (langue) des caractères asiatiques formatés.

```csharp
public int LocaleIdFarEast { get; set; }
```

## Remarques

Pour la liste des identifiants de paramètres régionaux, voir https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Exemples

Montre comment insérer et formater du texte dans une langue d'Extrême-Orient.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Spécifiez les paramètres de police que le générateur de documents appliquera à tout texte qu'il insère.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Nommez les équivalents « FarEast » pour notre police et nos paramètres régionaux.
// Si le générateur insère des caractères asiatiques avec cette configuration de police, alors chaque exécution qui contient
// ces caractères seront affichés en utilisant la police/les paramètres régionaux « FarEast » au lieu de la valeur par défaut.
// Cela peut être utile lorsqu'une police occidentale n'a pas de représentations idéales pour les caractères asiatiques.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// Ce texte sera affiché dans la police/les paramètres régionaux par défaut.
builder.Writeln("Hello world!");

// Étant donné qu'il s'agit de caractères asiatiques, cette exécution appliquera nos équivalents de police/localisation « FarEast ».
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

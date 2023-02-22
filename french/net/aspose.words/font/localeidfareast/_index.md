---
title: Font.LocaleIdFarEast
second_title: Référence de l'API Aspose.Words pour .NET
description: Font propriété. Obtient ou définit lidentifiant de paramètres régionaux langue des caractères asiatiques formatés.
type: docs
weight: 220
url: /fr/net/aspose.words/font/localeidfareast/
---
## Font.LocaleIdFarEast property

Obtient ou définit l'identifiant de paramètres régionaux (langue) des caractères asiatiques formatés.

```csharp
public int LocaleIdFarEast { get; set; }
```

### Remarques

Pour la liste des identifiants de paramètres régionaux, voir https://msdn.microsoft.com/en-us/library/cc233965.aspx

### Exemples

Montre comment insérer et formater du texte dans une langue d'Extrême-Orient.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Spécifiez les paramètres de police que le générateur de document appliquera à tout texte qu'il insère.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Nommez les équivalents "FarEast" pour notre police et nos paramètres régionaux.
// Si le générateur insère des caractères asiatiques avec cette configuration de police, alors chaque exécution contenant
// ces caractères les afficheront en utilisant la police/locale "FarEast" au lieu de la valeur par défaut.
// Cela peut être utile lorsqu'une police occidentale n'a pas de représentations idéales pour les caractères asiatiques.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// Ce texte sera affiché dans la police/locale par défaut.
builder.Writeln("Hello world!");

// Puisqu'il s'agit de caractères asiatiques, cette exécution appliquera nos équivalents police/locale "FarEast".
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../font/)
* Assemblée [Aspose.Words](../../../)



---
title: Font.NameFarEast
second_title: Référence de l'API Aspose.Words pour .NET
description: Font propriété. Renvoie ou définit un nom de police dAsie de lEst.
type: docs
weight: 260
url: /fr/net/aspose.words/font/namefareast/
---
## Font.NameFarEast property

Renvoie ou définit un nom de police d'Asie de l'Est.

```csharp
public string NameFarEast { get; set; }
```

### Exemples

Montre comment insérer et formater du texte dans une langue d'Extrême-Orient.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Spécifie les paramètres de police que le générateur de documents appliquera à tout texte qu'il insère.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Nommez les équivalents "FarEast" pour notre police et nos paramètres régionaux.
// Si le constructeur insère des caractères asiatiques avec cette configuration de police, alors chaque exécution contenant
// ces caractères les afficheront en utilisant la police/locale "FarEast" au lieu de la valeur par défaut.
// Cela peut être utile lorsqu'une police occidentale n'a pas de représentation idéale pour les caractères asiatiques.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// Ce texte sera affiché dans la police/locale par défaut.
builder.Writeln("Hello world!");

// Puisqu'il s'agit de caractères asiatiques, cette exécution appliquera nos équivalents de police/locale "Extrême-Orient".
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### Voir également

* property [Name](../name/)
* class [Font](../)
* espace de noms [Aspose.Words](../../font/)
* Assemblée [Aspose.Words](../../../)



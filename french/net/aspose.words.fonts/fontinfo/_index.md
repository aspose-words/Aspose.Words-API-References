---
title: Class FontInfo
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fonts.FontInfo classe. Spécifie des informations sur une police utilisée dans le document.
type: docs
weight: 2920
url: /fr/net/aspose.words.fonts/fontinfo/
---
## FontInfo class

Spécifie des informations sur une police utilisée dans le document.

Pour en savoir plus, visitez le[Travailler avec des polices](https://docs.aspose.com/words/net/working-with-fonts/) article documentaire.

```csharp
public class FontInfo
```

## Propriétés

| Nom | La description |
| --- | --- |
| [AltName](../../aspose.words.fonts/fontinfo/altname/) { get; set; } | Obtient ou définit le nom alternatif de la police. |
| [Charset](../../aspose.words.fonts/fontinfo/charset/) { get; set; } | Obtient ou définit le jeu de caractères pour la police. |
| [Family](../../aspose.words.fonts/fontinfo/family/) { get; set; } | Obtient ou définit la famille de polices à laquelle appartient cette police. |
| [IsTrueType](../../aspose.words.fonts/fontinfo/istruetype/) { get; set; } | Indique que cette police est une police TrueType ou OpenType par opposition à une police raster ou vectorielle. La valeur par défaut est`vrai` . |
| [Name](../../aspose.words.fonts/fontinfo/name/) { get; } | Obtient le nom de la police. |
| [Panose](../../aspose.words.fonts/fontinfo/panose/) { get; set; } | Obtient ou définit le numéro de classification de la police PANOSE. |
| [Pitch](../../aspose.words.fonts/fontinfo/pitch/) { get; set; } | Le pas indique si la police est à pas fixe, espacée proportionnellement ou s'appuie sur un paramètre par défaut. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetEmbeddedFont](../../aspose.words.fonts/fontinfo/getembeddedfont/)(EmbeddedFontFormat, EmbeddedFontStyle) | Obtient un fichier de police intégré spécifique. |
| [GetEmbeddedFontAsOpenType](../../aspose.words.fonts/fontinfo/getembeddedfontasopentype/)(EmbeddedFontStyle) | Obtient un fichier de police incorporé au format OpenType. Les polices au format Embedded OpenType sont converties en OpenType. |

### Remarques

Vous ne créez pas directement des instances de cette classe. Utilisez le[`FontInfos`](../../aspose.words/documentbase/fontinfos/) propriété pour accéder à la collection de polices définie dans un document.

### Exemples

Montre comment imprimer les détails des polices présentes dans un document.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Imprime toutes les polices utilisées et inutilisées dans le document.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### Voir également

* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)



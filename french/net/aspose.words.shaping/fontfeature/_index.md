---
title: FontFeature Enum
linktitle: FontFeature
articleTitle: FontFeature
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Shaping.FontFeature, qui détaille l'utilisation des glyphes dans les polices pour le rendu des scripts. Améliorez vos connaissances en typographie dès aujourd'hui !
type: docs
weight: 6860
url: /fr/net/aspose.words.shaping/fontfeature/
---
## FontFeature enumeration

Les fonctionnalités fournissent des informations sur la manière dont les glyphes sont utilisés dans une police pour restituer un script. https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags

```csharp
public enum FontFeature
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| GlyphCompositionDecomposition | `1667460464` | Pour minimiser le nombre d'alternatives de glyphes, il est parfois souhaitable de décomposer le glyphe par défaut d'un caractère en deux ou plusieurs glyphes. De plus, il peut être préférable de composer les glyphes par défaut de deux ou plusieurs caractères en un seul glyphe pour un meilleur traitement des glyphes. Cette fonctionnalité permet une telle composition/décomposition. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#ccmp Balise OpenType équivalente : « ccmp » |
| StandardLigatures | `1818847073` | Remplace une séquence de glyphes par un seul glyphe, préféré à des fins typographiques. Cette fonctionnalité couvre les ligatures que le concepteur/fabricant juge devoir être utilisées dans des conditions normales. Balise OpenType équivalente : « liga » https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#liga |
| RequiredLigatures | `1919707495` | Remplace une séquence de glyphes par un seul glyphe, préféré à des fins typographiques. Cette fonctionnalité couvre les ligatures que le script détermine comme devant être utilisées dans des conditions normales. Cette fonctionnalité est importante pour certains scripts afin de garantir une formation correcte des glyphes. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#rlig Balise OpenType équivalente : « rlig » |
| ContextualLigatures | `1668049255` | Remplace une séquence de glyphes par un seul glyphe, ce qui est préférable à des fins typographiques. Contrairement à d'autres fonctionnalités de ligature, « clig » spécifie le contexte dans lequel la ligature est recommandée. Cette fonctionnalité est importante dans certaines conceptions d'écriture et pour les ligatures ornées. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#clig Balise OpenType équivalente : « clig » |
| DiscretionaryLigatures | `1684826471` | Remplace une séquence de glyphes par un seul glyphe, préféré à des fins typographiques. Cette fonctionnalité couvre les ligatures qui peuvent être utilisées pour un effet spécial, selon les préférences de l'utilisateur. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#dlig Balise OpenType équivalente : « dlig » |
| HistoricalLigatures | `1751935335` | Certaines ligatures étaient couramment utilisées dans le passé, mais semblent anachroniques aujourd'hui. Certaines polices incluent les formes historiques comme alternatives, elles peuvent donc être utilisées pour un effet « période ». Cette fonctionnalité remplace les formes par défaut (actuelles) par les alternatives historiques. https://docs.microsoft.com/en-us/typography/opentype/spec/features_fj#hlig Balise OpenType équivalente : « hlig » |
| ProportionalFigures | `1886287213` | Remplace les glyphes de figures définis sur des largeurs uniformes (tabulaires) par des glyphes correspondants définis sur des largeurs spécifiques aux glyphes (proportionnelles). https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-pnum Balise OpenType équivalente : 'pnum' |
| TabularFigures | `1953396077` | Remplace les glyphes de figures définis sur des largeurs proportionnelles par des glyphes correspondants définis sur des largeurs uniformes (tabulaires). Les largeurs tabulaires seront généralement la valeur par défaut, mais cela ne peut pas être supposé en toute sécurité. Bien sûr, cette fonctionnalité ne serait pas présente dans les conceptions à espacement fixe. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-tnum Balise OpenType équivalente : 'tnum' |
| LiningFigures | `1819178349` | Cette fonctionnalité transforme les figures non alignées sélectionnées en figures alignées. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#lnum Balise OpenType équivalente : 'lnum' |
| OldstyleFigures | `1869509997` | Cette fonctionnalité modifie les figures sélectionnées du style par défaut ou de ligne au format ancien. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#onum Balise OpenType équivalente : 'onum' |
| VerticalAlternates | `1986359924` | Transforme les glyphes par défaut en glyphes adaptés à la présentation verticale en mode d'écriture verticale. https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vert Balise OpenType équivalente : 'vert' |
| VerticalAlternatesAndRotation | `1987212338` | Remplace certains glyphes à largeur fixe (demi-largeur, tiers ou quart de largeur) ou à largeur proportionnelle (principalement latins ou katakana) par des formes adaptées à l'écriture verticale (c'est-à-dire tournées de 90 degrés dans le sens des aiguilles d'une montre). https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vrt2 Balise OpenType équivalente : 'vrt2' |
| StylisticSet01 | `1936928817` | Ensemble stylistique 1 En plus ou à la place des alternatives stylistiques des glyphes individuels (voir la fonctionnalité « sel »), certaines polices peuvent contenir des ensembles de variantes stylistiques de glyphes correspondant à des parties du jeu de caractères, par exemple plusieurs variantes pour les lettres minuscules dans une police latine. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-ss01---ss20 Balise OpenType équivalente : 'ss01' |
| StylisticSet02 | `1936928818` | Ensemble stylistique 2 Balise OpenType équivalente : 'ss02' |
| StylisticSet03 | `1936928819` | Ensemble stylistique 3 Balise OpenType équivalente : 'ss03' |
| StylisticSet04 | `1936928820` | Ensemble stylistique 4 Balise OpenType équivalente : 'ss04' |
| StylisticSet05 | `1936928821` | Ensemble stylistique 5 Balise OpenType équivalente : 'ss05' |
| StylisticSet06 | `1936928822` | Ensemble stylistique 6 Balise OpenType équivalente : 'ss06' |
| StylisticSet07 | `1936928823` | Ensemble stylistique 7 Balise OpenType équivalente : 'ss07' |
| StylisticSet08 | `1936928824` | Ensemble stylistique 8 Balise OpenType équivalente : 'ss08' |
| StylisticSet09 | `1936928825` | Ensemble stylistique 9 Balise OpenType équivalente : 'ss09' |
| StylisticSet10 | `1936929072` | Ensemble stylistique 10 Balise OpenType équivalente : 'ss10' |
| StylisticSet11 | `1936929073` | Ensemble stylistique 11 Balise OpenType équivalente : 'ss11' |
| StylisticSet12 | `1936929074` | Ensemble stylistique 12 Balise OpenType équivalente : 'ss12' |
| StylisticSet13 | `1936929075` | Ensemble stylistique 13 Balise OpenType équivalente : 'ss13' |
| StylisticSet14 | `1936929076` | Ensemble stylistique 14 Balise OpenType équivalente : 'ss14' |
| StylisticSet15 | `1936929077` | Ensemble stylistique 15 Balise OpenType équivalente : 'ss15' |
| StylisticSet16 | `1936929078` | Ensemble stylistique 16 Balise OpenType équivalente : 'ss16' |
| StylisticSet17 | `1936929079` | Ensemble stylistique 17 Balise OpenType équivalente : 'ss17' |
| StylisticSet18 | `1936929080` | Ensemble stylistique 18 Balise OpenType équivalente : 'ss18' |
| StylisticSet19 | `1936929081` | Ensemble stylistique 19 Balise OpenType équivalente : 'ss19' |
| StylisticSet20 | `1936929328` | Ensemble stylistique 20 Balise OpenType équivalente : 'ss20' |
| Kerning | `1801810542` | Ajuste l'espacement entre les glyphes, généralement pour assurer un espacement optiquement cohérent entre les glyphes. Bien qu'une police de caractères bien conçue présente un espacement inter-glyphes globalement cohérent, certaines combinaisons de glyphes nécessitent un ajustement pour une meilleure lisibilité. Outre l'ajustement standard dans le sens horizontal, cette fonctionnalité peut fournir des données de crénage dépendant de la taille via des tables de périphériques, un crénage « cross-stream » dans le sens Y du texte et un ajustement du placement des glyphes indépendamment de l'ajustement avancé. Notez que cette fonctionnalité peut s'appliquer à des séries de plus de deux glyphes et ne serait pas utilisée dans les polices à espacement fixe. Notez également que cette fonctionnalité ne s'applique pas au texte défini verticalement. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#kern Balise OpenType équivalente : 'kern' |

### Voir également

* espace de noms [Aspose.Words.Shaping](../../aspose.words.shaping/)
* Assemblée [Aspose.Words](../../)

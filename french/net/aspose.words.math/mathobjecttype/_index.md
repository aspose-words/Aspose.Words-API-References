---
title: MathObjectType Enum
linktitle: MathObjectType
articleTitle: MathObjectType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Math.MathObjectType pour identifier et gérer facilement les types d'objets Office Math pour un traitement amélioré des documents.
type: docs
weight: 4800
url: /fr/net/aspose.words.math/mathobjecttype/
---
## MathObjectType enumeration

Spécifie le type d'un objet Office Math.

```csharp
public enum MathObjectType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| OMath | `0` | Instance de texte mathématique. |
| OMathPara | `1` | Paragraphe mathématique, ou zone mathématique d'affichage, qui contient un ou plusieursOMath éléments qui sont en mode d'affichage. |
| Accent | `2` | Fonction d'accentuation, composée d'une base et d'un signe diacritique combiné. |
| Bar | `3` | Fonction de barre, composée d'un argument de base et d'une barre supérieure ou inférieure. |
| BorderBox | `4` | Objet Border Box, constitué d'une bordure dessinée autour d'une instance de texte mathématique (comme une formule ou une équation) |
| Box | `5` | Objet Box, qui est utilisé pour regrouper les composants d'une équation ou d'une autre instance de texte mathématique. |
| Delimiter | `6` | Objet délimiteur, composé de délimiteurs ouvrants et fermants (tels que des parenthèses, des accolades, des crochets et des barres verticales) et d'un élément contenu à l'intérieur. |
| Degree | `7` | Diplôme en radical mathématique. |
| Argument | `8` | Objet argument. Englobe les entités Office Math utilisées comme arguments d'autres entités Office Math. |
| Array | `9` | Objet tableau, composé d'une ou plusieurs équations, expressions ou autres textes mathématiques, qui peuvent être justifiés verticalement comme une unité par rapport au texte environnant sur la ligne. |
| Fraction | `10` | Objet Fraction, composé d'un numérateur et d'un dénominateur séparés par une barre de fraction. |
| Denominator | `11` | Dénominateur d'un objet fractionnaire. |
| Numerator | `12` | Numérateur de l'objet Fraction. |
| Function | `13` | Objet Function-Apply, qui se compose d'un nom de fonction et d'un élément d'argument sur lequel on agit. |
| FunctionName | `14` | Nom de la fonction. Par exemple, les noms de fonction sont sin et cos. |
| GroupCharacter | `15` | Objet de groupe-caractère, constitué d'un caractère dessiné au-dessus ou au-dessous du texte, souvent dans le but de regrouper visuellement des éléments |
| Limit | `16` | Limite inférieure de laLowerLimit objet et la limite supérieure de laUpperLimit fonction. |
| LowerLimit | `17` | Objet de limite inférieure, composé de texte sur la ligne de base et de texte de taille réduite immédiatement en dessous. |
| UpperLimit | `18` | Objet de limite supérieure, composé de texte sur la ligne de base et de texte de taille réduite immédiatement au-dessus. |
| Matrix | `19` | Objet matriciel, constitué d'un ou plusieurs éléments disposés sur une ou plusieurs lignes et une ou plusieurs colonnes. |
| MatrixRow | `20` | Ligne unique de la matrice. |
| NAry | `21` | Objet n-aire, composé d'un objet n-aire, d'une base (ou opérande) et de limites supérieure et inférieure facultatives. |
| Phantom | `22` | Objet fantôme. |
| Radical | `23` | Objet radical, composé d'un radical, d'un élément de base et d'un degré optionnel. |
| SubscriptPart | `24` | Indice de l'objet qui peut avoir une partie en indice. |
| SuperscriptPart | `25` | Exposant de l'objet exposant. |
| PreSubSuperscript | `26` | Objet pré-sous-exposant, qui se compose d'un élément de base et d'un indice et d'un exposant placés à gauche de la base. |
| Subscript | `27` | Objet Subscript, qui se compose d'un élément de base et d'un script de taille réduite placé en dessous et à droite. |
| SubSuperscript | `28` | Objet sous-exposant, qui se compose d'un élément de base, d'un script de taille réduite placé en dessous et à droite, et d'un script de taille réduite placé au-dessus et à droite. |
| Supercript | `29` | Objet Superscript, qui se compose d'un élément de base et d'un script de taille réduite placé au-dessus et à droite. |

## Exemples

Montre comment imprimer la structure des nœuds de chaque nœud mathématique de bureau dans un document.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // Lorsque nous obtenons un nœud composite pour accepter un visiteur de document, le visiteur visite le nœud acceptant,
    // et parcourt ensuite tous les enfants du nœud de manière approfondie.
    // Le visiteur peut lire et modifier chaque nœud visité.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Parcourt l'arbre non binaire des nœuds enfants d'un nœud.
/// Crée une carte sous la forme d'une chaîne de tous les nœuds OfficeMath rencontrés et de leurs enfants.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
    /// Obtient le texte brut du document accumulé par le visiteur.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Appelé lorsqu'un nœud Run est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud OfficeMath est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
    {
        IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.MathObjectType);
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé après que tous les nœuds enfants d'un nœud OfficeMath ont été visités.
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Ajoutez une ligne au StringBuilder et indentez-la en fonction de la profondeur à laquelle se trouve le visiteur dans l'arborescence du document.
    /// </summary>
    /// <param name="texte"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideOfficeMath;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Voir également

* espace de noms [Aspose.Words.Math](../../aspose.words.math/)
* Assemblée [Aspose.Words](../../)

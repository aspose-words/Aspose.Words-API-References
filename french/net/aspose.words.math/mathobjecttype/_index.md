---
title: Enum MathObjectType
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Math.MathObjectType énumération. Spécifie le type dun objet Office Math.
type: docs
weight: 4110
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
| OMathPara | `1` | Paragraphe mathématique, ou zone d'affichage mathématique, qui contient un ou plusieursOMath éléments qui sont en mode d'affichage. |
| Accent | `2` | Fonction Accent, composée d'une base et d'un signe diacritique combiné. |
| Bar | `3` | Fonction Bar, composée d'un argument de base et d'une barre supérieure ou inférieure. |
| BorderBox | `4` | Objet Border Box, constitué d'une bordure dessinée autour d'une instance de texte mathématique (comme une formule ou une équation) |
| Box | `5` | Objet Box, utilisé pour regrouper les composants d'une équation ou d'une autre instance de texte mathématique. |
| Delimiter | `6` | Objet Delimiter, composé de délimiteurs ouvrants et fermants (tels que des parenthèses, des accolades , des crochets et des barres verticales) et d'un élément contenu à l'intérieur. |
| Degree | `7` | Diplôme dans le radical mathématique. |
| Argument | `8` | Objet argument. Entoure les entités Office Math lorsqu’elles sont utilisées comme arguments pour d’autres entités Office Math. |
| Array | `9` | Objet tableau, composé d'une ou plusieurs équations, expressions ou autres passages de texte mathématique qui peuvent être justifiés verticalement en tant qu'unité par rapport au texte environnant sur la ligne. |
| Fraction | `10` | Objet Fraction, composé d'un numérateur et d'un dénominateur séparés par une barre de fraction. |
| Denominator | `11` | Dénominateur d'un objet fraction. |
| Numerator | `12` | Numérateur de l'objet Fraction. |
| Function | `13` | Objet Function-Apply, qui se compose d'un nom de fonction et d'un élément d'argument sur lequel on agit. |
| FunctionName | `14` | Nom de la fonction. Par exemple, les noms de fonctions sont sin et cos. |
| GroupCharacter | `15` | Objet Group-Character, constitué d'un caractère dessiné au-dessus ou en dessous du texte, souvent dans le but de regrouper visuellement les éléments |
| Limit | `16` | Limite inférieure duLowerLimit objet et la limite supérieure duUpperLimit fonction. |
| LowerLimit | `17` | Objet Lower-Limit, composé de texte sur la ligne de base et de texte de taille réduite immédiatement en dessous. |
| UpperLimit | `18` | Objet Upper-Limit, composé de texte sur la ligne de base et de texte de taille réduite immédiatement au-dessus. |
| Matrix | `19` | Objet matriciel, composé d'un ou plusieurs éléments disposés en une ou plusieurs lignes et une ou plusieurs colonnes. |
| MatrixRow | `20` | Ligne unique de la matrice. |
| NAry | `21` | Objet N-aire, composé d'un objet n-aire, d'une base (ou opérande) et de limites supérieure et inférieure facultatives. |
| Phantom | `22` | Objet fantôme. |
| Radical | `23` | Objet radical, composé d'un radical, d'un élément de base et d'un degré facultatif . |
| SubscriptPart | `24` | Indice de l'objet pouvant avoir une partie indice. |
| SuperscriptPart | `25` | Exposant de l'objet exposant. |
| PreSubSuperscript | `26` | Objet Pre-Sub-Superscript, qui se compose d'un élément de base et d'un indice et d'un exposant placés à gauche de la base. |
| Subscript | `27` | Objet Indice, composé d'un élément de base et d'un script de taille réduite placé en bas et à droite. |
| SubSuperscript | `28` | Objet sous-exposant, composé d'un élément de base, d'un script de taille réduite placé en bas et à droite, et d'un script de taille réduite placé au-dessus et à droite. |
| Supercript | `29` | Objet Superscript, composé d'un élément de base et d'un script de taille réduite placé au-dessus et à droite. |

### Exemples

Montre comment imprimer la structure de chaque nœud mathématique de bureau dans un document.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // Lorsque nous obtenons qu'un nœud composite accepte un visiteur de document, le visiteur visite le nœud accepteur,
    // puis parcourt tous les enfants du nœud en profondeur.
    // Le visiteur peut lire et modifier chaque nœud visité.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Parcourt l'arborescence non binaire des nœuds enfants d'un nœud.
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
    /// Ajoutez une ligne au StringBuilder et indentez-la en fonction de la profondeur du visiteur dans l'arborescence du document.
    /// </summary>
    /// <param name="text"></param>
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



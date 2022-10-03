---
title: FieldEQ
second_title: Référence de l'API Aspose.Words pour .NET
description: Implémente le champ EQ.
type: docs
weight: 1680
url: /fr/net/aspose.words.fields/fieldeq/
---
## FieldEQ class

Implémente le champ EQ.

```csharp
public class FieldEQ : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldEQ](fieldeq/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtient le nœud qui représente la fin du champ. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtient un[`FieldFormat`](../fieldformat/) objet qui fournit un accès typé au formatage du champ. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtient ou définit le LCID du champ. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtient le nœud qui représente le séparateur de champs. Peut être null. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtient le nœud qui représente le début du champ. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtient le type de champ Microsoft Word. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code de champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie **nul** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update/)() | Effectue la mise à jour du champ. Lance si le champ est déjà mis à jour. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Effectue une mise à jour du champ. Lance si le champ est déjà mis à jour. |

### Exemples

Montre comment utiliser le champ EQ pour afficher diverses équations mathématiques.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Un champ EQ affiche une équation mathématique composée d'un ou plusieurs éléments.
    // Chaque élément prend la forme suivante : [switch][options][arguments].
    // Il peut y avoir un commutateur et plusieurs options possibles.
    // Les arguments sont un ensemble de valeurs séparées par des virgules entourées d'accolades.

    // Ici, nous utilisons un générateur de document pour insérer un champ EQ, avec un commutateur "\f", qui correspond à "Fraction".
    // Nous passerons les valeurs 1 et 4 en arguments, et nous n'utiliserons aucune option.
    // Ce champ affichera une fraction avec 1 comme numérateur et 4 comme dénominateur.
    FieldEQ field = InsertFieldEQ(builder, @"\f(1,4)");

    Assert.AreEqual(@" EQ \f(1,4)", field.GetFieldCode());

    // Un champ EQ peut contenir plusieurs éléments placés séquentiellement.
    // Nous pouvons également imbriquer des éléments les uns dans les autres en plaçant les éléments internes
    // à l'intérieur des parenthèses d'arguments des éléments extérieurs.
    // Nous pouvons trouver la liste complète des commutateurs, ainsi que leurs utilisations ici :
    // https://blogs.msdn.microsoft.com/murrays/2018/01/23/microsoft-word-eq-field/

    // Vous trouverez ci-dessous des applications de neuf commutateurs de champ EQ différents que nous pouvons utiliser pour créer différents types d'objets.
    // 1 - Commutateur de tableau "\a", aligné à gauche, 2 colonnes, 3 points d'espacement horizontal et vertical :
    InsertFieldEQ(builder, @"\a \al \co2 \vs3 \hs3(4x,- 4y,-4x,+ y)");

    // 2 - Commutateur de parenthèse "\b", caractère de parenthèse "[", pour entourer le contenu d'un ensemble d'accolades :
    // Notez que nous imbriquons un tableau à l'intérieur des crochets, qui ressemblera à une matrice dans la sortie.
    InsertFieldEQ(builder, @"\b \bc\[ (\a \al \co3 \vs3 \hs3(1,0,0,0,1,0,0,0,1))");

    // 3 - Commutateur de déplacement "\d", déplaçant le texte "B" de 30 espaces à droite de "A", affichant l'écart sous forme de soulignement :
    InsertFieldEQ(builder, @"A \d \fo30 \li() B");

    // 4 - Formule composée de fractions multiples :
    InsertFieldEQ(builder, @"\f(d,dx)(u + v) = \f(du,dx) + \f(dv,dx)");

    // 5 - Commutateur intégral "\i", avec un symbole de sommation :
    InsertFieldEQ(builder, @"\i \su(n=1,5,n)");

    // 6 - Commutateur de liste "\l":
    InsertFieldEQ(builder, @"\l(1,1,2,3,n,8,13)");

    // 7 - Commutateur radical "\r", affichant une racine cubique de x :
    InsertFieldEQ(builder, @"\r (3,x)");

    // 8 - Commutateur indice/exposant "/s", d'abord en exposant puis en indice :
    InsertFieldEQ(builder, @"\s \up8(Superscript) Text \s \do8(Subscript)");

    // 9 - Box switch "\x", avec des lignes en haut, en bas, à gauche et à droite de l'entrée :
    InsertFieldEQ(builder, @"\x \to \bo \le \ri(5)");

    // Quelques combinaisons plus complexes.
    InsertFieldEQ(builder, @"\a \ac \vs1 \co1(lim,n→∞) \b (\f(n,n2 + 12) + \f(n,n2 + 22) + ... + \f(n,n2 + n2))");
    InsertFieldEQ(builder, @"\i (,,  \b(\f(x,x2 + 3x + 2))) \s \up10(2)");
    InsertFieldEQ(builder, @"\i \in( tan x, \s \up2(sec x), \b(\r(3) )\s \up4(t) \s \up7(2)  dt)");

    doc.Save(ArtifactsDir + "Field.EQ.docx");

/// <summary>
/// Utilisez un générateur de document pour insérer un champ EQ, définir ses arguments et commencer un nouveau paragraphe.
/// </summary>
private static FieldEQ InsertFieldEQ(DocumentBuilder builder, string args)
{
    FieldEQ field = (FieldEQ)builder.InsertField(FieldType.FieldEquation, true);
    builder.MoveTo(field.Separator);
    builder.Write(args);
    builder.MoveTo(field.Start.ParentNode);

    builder.InsertParagraph();
    return field;
}
```

### Voir également

* class [Field](../field/)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

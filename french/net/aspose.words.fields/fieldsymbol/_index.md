---
title: FieldSymbol
second_title: Référence de l'API Aspose.Words pour .NET
description: Implémente un champ SYMBOL.
type: docs
weight: 2310
url: /fr/net/aspose.words.fields/fieldsymbol/
---
## FieldSymbol class

Implémente un champ SYMBOL.

```csharp
public class FieldSymbol : Field
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FieldSymbol](fieldsymbol)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [CharacterCode](../../aspose.words.fields/fieldsymbol/charactercode) { get; set; } | Obtient ou définit la valeur du point de code du caractère en décimal ou hexadécimal. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Obtient le texte qui représente le résultat du champ affiché. |
| [DontAffectsLineSpacing](../../aspose.words.fields/fieldsymbol/dontaffectslinespacing) { get; set; } | Obtient ou définit si le caractère récupéré par le champ affecte l'interligne du paragraphe. |
| [End](../../aspose.words.fields/field/end) { get; } | Obtient le nœud qui représente la fin du champ. |
| [FontName](../../aspose.words.fields/fieldsymbol/fontname) { get; set; } | Obtient ou définit le nom de la police du caractère récupéré par le champ. |
| [FontSize](../../aspose.words.fields/fieldsymbol/fontsize) { get; set; } | Obtient ou définit la taille en points de la police du caractère récupéré par le champ. |
| [Format](../../aspose.words.fields/field/format) { get; } | Obtient un[`FieldFormat`](../fieldformat) objet qui fournit un accès typé au formatage du champ. |
| [IsAnsi](../../aspose.words.fields/fieldsymbol/isansi) { get; set; } | Obtient ou définit si le code de caractère est interprété comme la valeur d'un caractère ANSI. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Obtient ou définit si le résultat actuel du champ n'est plus correct (périmé) en raison d'autres modifications apportées au document. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [IsShiftJis](../../aspose.words.fields/fieldsymbol/isshiftjis) { get; set; } | Obtient ou définit si le code de caractère est interprété comme la valeur d'un caractère SHIFT-JIS. |
| [IsUnicode](../../aspose.words.fields/fieldsymbol/isunicode) { get; set; } | Obtient ou définit si le code de caractère est interprété comme la valeur d'un caractère Unicode. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Obtient ou définit le LCID du champ. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Obtient ou définit le texte qui se trouve entre le séparateur de champ et la fin du champ. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Obtient le nœud qui représente le séparateur de champs. Peut être null. |
| [Start](../../aspose.words.fields/field/start) { get; } | Obtient le nœud qui représente le début du champ. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Obtient le type de champ Microsoft Word. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code de champ et le résultat du champ des champs enfants sont inclus. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [Remove](../../aspose.words.fields/field/remove)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie son paragraphe parent. Si le champ est déjà supprimé, renvoie **nul** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Effectue la dissociation du champ. |
| [Update](../../aspose.words.fields/field/update)() | Effectue la mise à jour du champ. Lance si le champ est déjà mis à jour. |
| [Update](../../aspose.words.fields/field/update)(bool) | Effectue une mise à jour du champ. Lance si le champ est déjà mis à jour. |

### Remarques

Récupère le caractère dont la valeur du point de code est spécifiée en décimal ou en hexadécimal.

### Exemples

Montre comment utiliser le champ SYMBOLE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous trois manières d'utiliser un champ SYMBOLE pour afficher un seul caractère.
// 1 - Ajouter un champ SYMBOLE qui affiche le symbole © (Copyright), spécifié par un code de caractère ANSI :
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// Le code de caractère ANSI "U+00A9", ou "169" sous forme entière, est réservé au symbole de copyright.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - Ajoutez un champ SYMBOLE qui affiche le symbole ∞ (Infini), et modifiez son apparence :
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// En Unicode, le symbole de l'infini occupe le code "221E".
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// Changer la police de notre symbole après avoir utilisé la table des caractères Windows
// pour s'assurer que la police peut représenter ce symbole.
field.FontName = "Calibri";
field.FontSize = "24";

// Nous pouvons définir cet indicateur pour les grands symboles afin qu'ils ne poussent pas le reste du texte sur leur ligne.
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - Ajouter un champ SYMBOLE qui affiche le caractère あ,
// avec une police prenant en charge la page de codes Shift-JIS (Windows-932) :
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);
field.FontName = "MS Gothic";
field.CharacterCode = 0x82A0.ToString();
field.IsShiftJis = true;

Assert.AreEqual(" SYMBOL  33440 \\f \"MS Gothic\" \\j", field.GetFieldCode());

builder.Write("Line 3");

doc.Save(ArtifactsDir + "Field.SYMBOL.docx");
```

### Voir également

* class [Field](../field)
* espace de noms [Aspose.Words.Fields](../../aspose.words.fields)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

---
title: FieldSymbol.IsShiftJis
linktitle: IsShiftJis
articleTitle: IsShiftJis
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldSymbol IsShiftJis : gérez facilement les codes de caractères SHIFTJIS pour une gestion améliorée des données et une interprétation transparente des caractères.
type: docs
weight: 70
url: /fr/net/aspose.words.fields/fieldsymbol/isshiftjis/
---
## FieldSymbol.IsShiftJis property

Obtient ou définit si le code de caractère est interprété comme la valeur d'un caractère SHIFT-JIS.

```csharp
public bool IsShiftJis { get; set; }
```

## Exemples

Montre comment utiliser le champ SYMBOLE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous trois façons d'utiliser un champ SYMBOL pour afficher un seul caractère.
// 1 - Ajoutez un champ SYMBOL qui affiche le symbole © (Copyright), spécifié par un code de caractère ANSI :
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// Le code de caractère ANSI « U+00A9 », ou « 169 » sous forme entière, est réservé au symbole de copyright.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - Ajoutez un champ SYMBOL qui affiche le symbole ∞ (Infini) et modifiez son apparence :
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// En Unicode, le symbole de l'infini occupe le code « 221E ».
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// Changer la police de notre symbole après avoir utilisé la table des caractères Windows
// pour garantir que la police peut représenter ce symbole.
field.FontName = "Calibri";
field.FontSize = "24";

// Nous pouvons définir cet indicateur pour les symboles hauts afin qu'ils ne poussent pas le reste du texte sur leur ligne.
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - Ajouter un champ SYMBOL qui affiche le caractère あ,
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

* class [FieldSymbol](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)

---
title: FieldSymbol.DontAffectsLineSpacing
linktitle: DontAffectsLineSpacing
articleTitle: DontAffectsLineSpacing
second_title: Aspose.Words pour .NET
description: FieldSymbol DontAffectsLineSpacing propriété. Obtient ou définit si le caractère récupéré par le champ affecte linterligne du paragraphe en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldsymbol/dontaffectslinespacing/
---
## FieldSymbol.DontAffectsLineSpacing property

Obtient ou définit si le caractère récupéré par le champ affecte l'interligne du paragraphe.

```csharp
public bool DontAffectsLineSpacing { get; set; }
```

## Exemples

Montre comment utiliser le champ SYMBOLE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous trois façons d'utiliser un champ SYMBOL pour afficher un seul caractère.
// 1 - Ajoutez un champ SYMBOLE qui affiche le symbole © (Copyright), spécifié par un code de caractère ANSI :
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// Le code de caractère ANSI "U+00A9", ou "169" sous forme entière, est réservé au symbole de droit d'auteur.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - Ajoutez un champ SYMBOLE qui affiche le symbole ∞ (Infini), et modifiez son apparence :
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// En Unicode, le symbole de l'infini occupe le code "221E".
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// Change la police de notre symbole après avoir utilisé la table de caractères Windows
// pour garantir que la police peut représenter ce symbole.
field.FontName = "Calibri";
field.FontSize = "24";

// Nous pouvons définir cet indicateur pour les symboles de grande taille afin qu'ils ne poussent pas le reste du texte sur leur ligne.
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - Ajout d'un champ SYMBOLE qui affiche le caractère あ,
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

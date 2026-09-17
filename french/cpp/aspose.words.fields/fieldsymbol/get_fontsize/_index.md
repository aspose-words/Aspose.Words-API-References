---
title: "Aspose::Words::Fields::FieldSymbol::get_FontSize méthode"
linktitle: "get_FontSize"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldSymbol::get_FontSize méthode. Obtient ou définit la taille en points de la police du caractère récupéré par le champ en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.fields/fieldsymbol/get_fontsize/
---
## FieldSymbol::get_FontSize method


Obtient ou définit la taille en points de la police du caractère récupéré par le champ.

```cpp
System::String Aspose::Words::Fields::FieldSymbol::get_FontSize()
```


## Exemples



Montre comment utiliser le champ SYMBOL.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Voici trois façons d'utiliser un champ SYMBOL pour afficher un seul caractère.
// 1 -  Ajoutez un champ SYMBOL qui affiche le symbole © (Copyright), spécifié par un code de caractère ANSI :
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// Le code de caractère ANSI "U+00A9", ou "169" sous forme entière, est réservé au symbole de copyright.
field->set_CharacterCode(System::Convert::ToString(0x00a9));
field->set_IsAnsi(true);

ASSERT_EQ(u" SYMBOL  169 \\a", field->GetFieldCode());

builder->Writeln(u" Line 1");

// 2 -  Ajoutez un champ SYMBOL qui affiche le symbole ∞ (Infinity), et modifiez son apparence :
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// En Unicode, le symbole d'infini occupe le code "221E".
field->set_CharacterCode(System::Convert::ToString(0x221E));
field->set_IsUnicode(true);

// Changez la police de notre symbole après avoir utilisé le Windows Character Map.
// afin de garantir que la police puisse représenter ce symbole.
field->set_FontName(u"Calibri");
field->set_FontSize(u"24");

// Nous pouvons définir ce drapeau pour les symboles hauts afin qu'ils ne repoussent pas le reste du texte sur leur ligne.
field->set_DontAffectsLineSpacing(true);

ASSERT_EQ(u" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field->GetFieldCode());

builder->Writeln(u"Line 2");

// 3 -  Ajoutez un champ SYMBOL qui affiche le caractère あ,
// avec une police qui prend en charge la page de code Shift-JIS (Windows-932) :
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));
field->set_FontName(u"MS Gothic");
field->set_CharacterCode(System::Convert::ToString(0x82A0));
field->set_IsShiftJis(true);

ASSERT_EQ(u" SYMBOL  33440 \\f \"MS Gothic\" \\j", field->GetFieldCode());

builder->Write(u"Line 3");

doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## Voir aussi

* Class [FieldSymbol](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)

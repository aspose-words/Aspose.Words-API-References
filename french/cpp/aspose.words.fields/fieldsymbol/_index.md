---
title: "Aspose::Words::Fields::FieldSymbol classe"
linktitle: "FieldSymbol"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldSymbol classe. Implémente un champ SYMBOL. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 98000
url: /fr/cpp/aspose.words.fields/fieldsymbol/
---
## FieldSymbol class


Implémente un champ SYMBOL. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldSymbol : public Aspose::Words::Fields::Field,
                    public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_CharacterCode](./get_charactercode/)() | Obtient ou définit la valeur du point de code du caractère en décimal ou en hexadécimal. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_DontAffectsLineSpacing](./get_dontaffectslinespacing/)() | Obtient ou définit si le caractère récupéré par le champ affecte l'interligne du paragraphe. |
| [get_End](../field/get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_FontName](./get_fontname/)() | Obtient ou définit le nom de la police du caractère récupéré par le champ. |
| [get_FontSize](./get_fontsize/)() | Obtient ou définit la taille en points de la police du caractère récupéré par le champ. |
| [get_Format](../field/get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_IsAnsi](./get_isansi/)() | Obtient ou définit si le code du caractère est interprété comme la valeur d'un caractère ANSI. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_IsShiftJis](./get_isshiftjis/)() | Obtient ou définit si le code du caractère est interprété comme la valeur d'un caractère SHIFT-JIS. |
| [get_IsUnicode](./get_isunicode/)() | Obtient ou définit si le code du caractère est interprété comme la valeur d'un caractère Unicode. |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_Separator](../field/get_separator/)() | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| virtual [get_Type](../field/get_type/)() const | Obtient le type de champ Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_CharacterCode](./set_charactercode/)(const System::String\&) | Mutateur pour [Aspose::Words::Fields::FieldSymbol::get_CharacterCode](./get_charactercode/). |
| [set_DontAffectsLineSpacing](./set_dontaffectslinespacing/)(bool) | Mutateur pour [Aspose::Words::Fields::FieldSymbol::get_DontAffectsLineSpacing](./get_dontaffectslinespacing/). |
| [set_FontName](./set_fontname/)(const System::String\&) | Mutateur pour [Aspose::Words::Fields::FieldSymbol::get_FontName](./get_fontname/). |
| [set_FontSize](./set_fontsize/)(const System::String\&) | Mutateur pour [Aspose::Words::Fields::FieldSymbol::get_FontSize](./get_fontsize/). |
| [set_IsAnsi](./set_isansi/)(bool) | Mutateur pour [Aspose::Words::Fields::FieldSymbol::get_IsAnsi](./get_isansi/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_IsShiftJis](./set_isshiftjis/)(bool) | Mutateur pour [Aspose::Words::Fields::FieldSymbol::get_IsShiftJis](./get_isshiftjis/). |
| [set_IsUnicode](./set_isunicode/)(bool) | Mutateur pour [Aspose::Words::Fields::FieldSymbol::get_IsUnicode](./get_isunicode/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |

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

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)

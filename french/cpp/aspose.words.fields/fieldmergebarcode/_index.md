---
title: "Aspose::Words::Fields::FieldMergeBarcode classe"
linktitle: "FieldMergeBarcode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldMergeBarcode classe. Implémente le champ MERGEBARCODE. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 66000
url: /fr/cpp/aspose.words.fields/fieldmergebarcode/
---
## FieldMergeBarcode class


Implémente le champ MERGEBARCODE. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldMergeBarcode : public Aspose::Words::Fields::Field,
                          public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                          public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_AddStartStopChar](./get_addstartstopchar/)() | Obtient si l’on doit ajouter les caractères de début/fin pour les types de code-barres NW7 et CODE39. |
| [get_BackgroundColor](./get_backgroundcolor/)() | Obtient la couleur d'arrière-plan du symbole du code-barres. Les valeurs valides sont dans la plage [0, 0xFFFFFF]. |
| [get_BarcodeType](./get_barcodetype/)() | Obtient le type de code-barres (QR, etc.). |
| [get_BarcodeValue](./get_barcodevalue/)() | Obtient la valeur du code-barres. |
| [get_CaseCodeStyle](./get_casecodestyle/)() | Gets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_DisplayText](./get_displaytext/)() | Obtient si l’on doit afficher les données du code-barres (texte) avec l'image. |
| [get_End](./get_end/)() override | Obtient le nœud qui représente la fin du champ. |
| [get_End](../field/get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() | Obtient le niveau de correction d'erreur du QR Code. Les valeurs valides sont [0, 3]. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_FixCheckDigit](./get_fixcheckdigit/)() | Obtient si l’on doit corriger le chiffre de contrôle s’il est invalide. |
| [get_ForegroundColor](./get_foregroundcolor/)() | Obtient la couleur de premier plan du symbole du code-barres. Les valeurs valides sont dans la plage [0, 0xFFFFFF]. |
| [get_Format](../field/get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_PosCodeStyle](./get_poscodestyle/)() | Gets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_ScalingFactor](./get_scalingfactor/)() | Obtient un facteur d'échelle pour le symbole. La valeur est en points de pourcentage entiers et les valeurs valides sont [10, 1000]. |
| [get_Separator](./get_separator/)() override | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_Start](./get_start/)() override | Obtient le nœud qui représente le début du champ. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| [get_SymbolHeight](./get_symbolheight/)() | Obtient la hauteur du symbole. Les unités sont en TWIPS (1/1440 pouce). |
| [get_SymbolRotation](./get_symbolrotation/)() | Obtient la rotation du symbole du code-barres. Les valeurs valides sont [0, 3]. |
| virtual [get_Type](../field/get_type/)() const | Obtient le type de champ Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | Définit si l’on doit ajouter les caractères de début/fin pour les types de code-barres NW7 et CODE39. |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Définit la couleur d'arrière-plan du symbole du code-barres. Les valeurs valides sont dans la plage [0, 0xFFFFFF]. |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Définit le type de code-barres (QR, etc.). |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Définit la valeur du code-barres. |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | Sets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | Définit si l’on doit afficher les données du code-barres (texte) avec l'image. |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | Définit le niveau de correction d'erreur du QR Code. Les valeurs valides sont [0, 3]. |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Définit si l’on doit corriger le chiffre de contrôle s’il est invalide. |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Définit la couleur de premier plan du symbole du code-barres. Les valeurs valides sont dans la plage [0, 0xFFFFFF]. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | Sets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Définit un facteur d'échelle pour le symbole. La valeur est en points de pourcentage entiers et les valeurs valides sont [10, 1000]. |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Définit la hauteur du symbole. Les unités sont en TWIPS (1/1440 pouce). |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Définit la rotation du symbole de code-barres. Les valeurs valides sont [0, 3]. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |
## Voir aussi

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)

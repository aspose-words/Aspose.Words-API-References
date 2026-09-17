---
title: "Aspose::Words::Fields::BarcodeParameters classe"
linktitle: "BarcodeParameters"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::BarcodeParameters classe. Classe conteneur pour les paramètres de code-barres à transmettre à BarcodeGenerator. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class


Classe conteneur pour les paramètres de code-barres à transmettre à BarcodeGenerator. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class BarcodeParameters : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [BarcodeParameters](./barcodeparameters/)() |  |
| [get_AddStartStopChar](./get_addstartstopchar/)() const | Indique s'il faut ajouter les caractères de début/fin pour les types de code-barres NW7 et CODE39. |
| [get_BackgroundColor](./get_backgroundcolor/)() const | Couleur d'arrière-plan du code-barres (0x000000 - 0xFFFFFF) |
| [get_BarcodeType](./get_barcodetype/)() const | Type de code-barres. |
| [get_BarcodeValue](./get_barcodevalue/)() const | Données à encoder. |
| [get_CaseCodeStyle](./get_casecodestyle/)() const | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayText](./get_displaytext/)() const | Indique s'il faut afficher les données du code-barres (texte) avec l'image. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() const | Niveau de correction d'erreur du QR Code. Les valeurs valides sont [0, 3]. |
| [get_FacingIdentificationMark](./get_facingidentificationmark/)() const | Type d'une marque d'identification d'orientation (FIM). |
| [get_FixCheckDigit](./get_fixcheckdigit/)() const | Indique s'il faut corriger le chiffre de contrôle s'il est invalide. |
| [get_ForegroundColor](./get_foregroundcolor/)() const | Couleur de premier plan du code-barres (0x000000 - 0xFFFFFF) |
| [get_IsBookmark](./get_isbookmark/)() const | Indique si [PostalAddress](./get_postaladdress/) est le nom d'un signet. |
| [get_IsUSPostalAddress](./get_isuspostaladdress/)() const | Indique si [PostalAddress](./get_postaladdress/) est une adresse postale américaine. |
| [get_PosCodeStyle](./get_poscodestyle/)() const | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_PostalAddress](./get_postaladdress/)() const | Adresse postale du code-barres. |
| [get_ScalingFactor](./get_scalingfactor/)() const | Facteur d'échelle pour le symbole. La valeur est exprimée en points de pourcentage entiers et les valeurs valides sont [10, 1000]. |
| [get_SymbolHeight](./get_symbolheight/)() const | Hauteur de l'image du code-barres (en twips - 1/1440 pouces) |
| [get_SymbolRotation](./get_symbolrotation/)() const | Rotation du symbole du code-barres. Les valeurs valides sont [0, 3]. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | Indique s'il faut ajouter les caractères de début/fin pour les types de code-barres NW7 et CODE39. |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Couleur d'arrière-plan du code-barres (0x000000 - 0xFFFFFF) |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Type de code-barres. |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Données à encoder. |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | Indique s'il faut afficher les données du code-barres (texte) avec l'image. |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | Niveau de correction d'erreur du QR Code. Les valeurs valides sont [0, 3]. |
| [set_FacingIdentificationMark](./set_facingidentificationmark/)(const System::String\&) | Type d'une marque d'identification d'orientation (FIM). |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Indique s'il faut corriger le chiffre de contrôle s'il est invalide. |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Couleur de premier plan du code-barres (0x000000 - 0xFFFFFF) |
| [set_IsBookmark](./set_isbookmark/)(bool) | Indique si [PostalAddress](./get_postaladdress/) est le nom d'un signet. |
| [set_IsUSPostalAddress](./set_isuspostaladdress/)(bool) | Indique si [PostalAddress](./get_postaladdress/) est une adresse postale américaine. |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [set_PostalAddress](./set_postaladdress/)(const System::String\&) | Adresse postale du code-barres. |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Facteur d'échelle pour le symbole. La valeur est exprimée en points de pourcentage entiers et les valeurs valides sont [10, 1000]. |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Hauteur de l'image du code-barres (en twips - 1/1440 pouces) |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Rotation du symbole du code-barres. Les valeurs valides sont [0, 3]. |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)

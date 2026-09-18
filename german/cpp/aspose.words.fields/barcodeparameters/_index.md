---
title: "Aspose::Words::Fields::BarcodeParameters Klasse"
linktitle: "BarcodeParameters"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::BarcodeParameters Klasse. Containerklasse für Barcode-Parameter, die an BarcodeGenerator weitergereicht werden. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class


Container‑Klasse für Barcode‑Parameter, die an BarcodeGenerator weitergereicht werden. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class BarcodeParameters : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [BarcodeParameters](./barcodeparameters/)() |  |
| [get_AddStartStopChar](./get_addstartstopchar/)() const | Ob Start-/Stopp-Zeichen für die Barcode-Typen NW7 und CODE39 hinzugefügt werden sollen. |
| [get_BackgroundColor](./get_backgroundcolor/)() const | Barcode-Hintergrundfarbe (0x000000 - 0xFFFFFF) |
| [get_BarcodeType](./get_barcodetype/)() const | Barcode-Typ. |
| [get_BarcodeValue](./get_barcodevalue/)() const | Zu codierende Daten. |
| [get_CaseCodeStyle](./get_casecodestyle/)() const | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayText](./get_displaytext/)() const | Ob Barcode-Daten (Text) zusammen mit dem Bild angezeigt werden sollen. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() const | Fehlerkorrekturstufe des QR-Codes. Gültige Werte sind [0, 3]. |
| [get_FacingIdentificationMark](./get_facingidentificationmark/)() const | Typ eines Facing Identification Mark (FIM). |
| [get_FixCheckDigit](./get_fixcheckdigit/)() const | Ob die Prüfziffer korrigiert werden soll, wenn sie ungültig ist. |
| [get_ForegroundColor](./get_foregroundcolor/)() const | Barcode-Vordergrundfarbe (0x000000 - 0xFFFFFF) |
| [get_IsBookmark](./get_isbookmark/)() const | Ob [PostalAddress](./get_postaladdress/) der Name eines Lesezeichens ist. |
| [get_IsUSPostalAddress](./get_isuspostaladdress/)() const | Ob [PostalAddress](./get_postaladdress/) eine US-Postadresse ist. |
| [get_PosCodeStyle](./get_poscodestyle/)() const | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_PostalAddress](./get_postaladdress/)() const | Barcode-Postadresse. |
| [get_ScalingFactor](./get_scalingfactor/)() const | Skalierungsfaktor für das Symbol. Der Wert ist in ganzen Prozentpunkten angegeben und die gültigen Werte liegen zwischen [10, 1000]. |
| [get_SymbolHeight](./get_symbolheight/)() const | Barcode-Bildhöhe (in Twips – 1/1440 Zoll) |
| [get_SymbolRotation](./get_symbolrotation/)() const | Rotation des Barcode-Symbols. Gültige Werte sind [0, 3]. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | Ob Start-/Stopp-Zeichen für die Barcode-Typen NW7 und CODE39 hinzugefügt werden sollen. |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Barcode-Hintergrundfarbe (0x000000 - 0xFFFFFF) |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Barcode-Typ. |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Zu codierende Daten. |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | Ob Barcode-Daten (Text) zusammen mit dem Bild angezeigt werden sollen. |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | Fehlerkorrekturstufe des QR-Codes. Gültige Werte sind [0, 3]. |
| [set_FacingIdentificationMark](./set_facingidentificationmark/)(const System::String\&) | Typ eines Facing Identification Mark (FIM). |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Ob die Prüfziffer korrigiert werden soll, wenn sie ungültig ist. |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Barcode-Vordergrundfarbe (0x000000 - 0xFFFFFF) |
| [set_IsBookmark](./set_isbookmark/)(bool) | Ob [PostalAddress](./get_postaladdress/) der Name eines Lesezeichens ist. |
| [set_IsUSPostalAddress](./set_isuspostaladdress/)(bool) | Ob [PostalAddress](./get_postaladdress/) eine US-Postadresse ist. |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [set_PostalAddress](./set_postaladdress/)(const System::String\&) | Barcode-Postadresse. |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Skalierungsfaktor für das Symbol. Der Wert ist in ganzen Prozentpunkten angegeben und die gültigen Werte liegen zwischen [10, 1000]. |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Barcode-Bildhöhe (in Twips – 1/1440 Zoll) |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Rotation des Barcode-Symbols. Gültige Werte sind [0, 3]. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)

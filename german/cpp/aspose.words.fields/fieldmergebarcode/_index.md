---
title: "Aspose::Words::Fields::FieldMergeBarcode Klasse"
linktitle: "FieldMergeBarcode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldMergeBarcode Klasse. Implementiert das MERGEBARCODE-Feld. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 66000
url: /de/cpp/aspose.words.fields/fieldmergebarcode/
---
## FieldMergeBarcode class


Implementiert das MERGEBARCODE-Feld. Weitere Informationen finden Sie im [Arbeiten mit Feldern](https://docs.aspose.com/words/cpp/working-with-fields/) Dokumentationsartikel.

```cpp
class FieldMergeBarcode : public Aspose::Words::Fields::Field,
                          public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                          public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_AddStartStopChar](./get_addstartstopchar/)() | Ermittelt, ob Start-/Stopp-Zeichen für die Barcode-Typen NW7 und CODE39 hinzugefügt werden sollen. |
| [get_BackgroundColor](./get_backgroundcolor/)() | Ermittelt die Hintergrundfarbe des Barcode-Symbols. Gültige Werte liegen im Bereich [0, 0xFFFFFF]. |
| [get_BarcodeType](./get_barcodetype/)() | Ermittelt den Barcode-Typ (QR usw.). |
| [get_BarcodeValue](./get_barcodevalue/)() | Ermittelt den Barcode-Wert. |
| [get_CaseCodeStyle](./get_casecodestyle/)() | Gets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayResult](../field/get_displayresult/)() | Liefert den Text, der das angezeigte Feldresultat darstellt. |
| [get_DisplayText](./get_displaytext/)() | Ermittelt, ob Barcode-Daten (Text) zusammen mit dem Bild angezeigt werden sollen. |
| [get_End](./get_end/)() override | Liefert den Knoten, der das Feldende darstellt. |
| [get_End](../field/get_end/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() | Ermittelt das Fehlerkorrektur‑Level des QR‑Codes. Gültige Werte sind [0, 3]. |
| [get_FieldEnd](../field/get_fieldend/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldStart](../field/get_fieldstart/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_FixCheckDigit](./get_fixcheckdigit/)() | Ermittelt, ob die Prüfziffer korrigiert werden soll, wenn sie ungültig ist. |
| [get_ForegroundColor](./get_foregroundcolor/)() | Ermittelt die Vordergrundfarbe des Barcode-Symbols. Gültige Werte liegen im Bereich [0, 0xFFFFFF]. |
| [get_Format](../field/get_format/)() | Liefert ein [FieldFormat](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Feldes bietet. |
| [get_IsDirty](../field/get_isdirty/)() | Liefert oder setzt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [get_IsLocked](../field/get_islocked/)() | Liefert oder setzt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [get_LocaleId](../field/get_localeid/)() | Liefert oder setzt die LCID des Feldes. |
| [get_PosCodeStyle](./get_poscodestyle/)() | Gets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_Result](../field/get_result/)() | Liefert oder setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [get_ScalingFactor](./get_scalingfactor/)() | Ermittelt einen Skalierungsfaktor für das Symbol. Der Wert ist in ganzen Prozentpunkten angegeben und gültige Werte liegen zwischen [10, 1000]. |
| [get_Separator](./get_separator/)() override | Liefert den Knoten, der das Feldtrennzeichen darstellt. Kann **null** sein. |
| [get_Start](./get_start/)() override | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_Start](../field/get_start/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_SymbolHeight](./get_symbolheight/)() | Ermittelt die Höhe des Symbols. Die Einheit ist TWIPS (1/1440 Zoll). |
| [get_SymbolRotation](./get_symbolrotation/)() | Ermittelt die Drehung des Barcode-Symbols. Gültige Werte sind [0, 3]. |
| virtual [get_Type](../field/get_type/)() const | Liefert den Microsoft‑Word-Feldtyp. |
| [GetFieldCode](../field/getfieldcode/)() | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldresultat von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Feldes das letzte Kind seines übergeordneten Knotens ist, gibt es den übergeordneten Absatz zurück. Wenn das Feld bereits entfernt wurde, gibt es **null** zurück. |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | Legt fest, ob Start-/Stopp-Zeichen für die Barcode-Typen NW7 und CODE39 hinzugefügt werden sollen. |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Legt die Hintergrundfarbe des Barcodesymbols fest. Gültige Werte liegen im Bereich [0, 0xFFFFFF]. |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Legt den Barcode-Typ fest (QR usw.). |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Legt den Barcode-Wert fest. |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | Sets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | Legt fest, ob Barcode-Daten (Text) zusammen mit dem Bild angezeigt werden. |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | Legt ein Fehlerkorrekturlevel für QR-Code fest. Gültige Werte sind [0, 3]. |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Legt fest, ob die Prüfziffer korrigiert werden soll, wenn sie ungültig ist. |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Legt die Vordergrundfarbe des Barcodesymbols fest. Gültige Werte liegen im Bereich [0, 0xFFFFFF]. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter für [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | Sets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter für [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Legt einen Skalierungsfaktor für das Symbol fest. Der Wert ist in ganzen Prozentpunkten angegeben und gültige Werte sind [10, 1000]. |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Legt die Höhe des Symbols fest. Die Einheit ist TWIPS (1/1440 Zoll). |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Legt die Drehung des Barcodesymbols fest. Gültige Werte sind [0, 3]. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Führt das Entlinken des Feldes aus. |
| [Update](../field/update/)() | Führt das Aktualisieren des Feldes aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
| [Update](../field/update/)(bool) | Führt ein Feld-Update aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
## Siehe auch

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)

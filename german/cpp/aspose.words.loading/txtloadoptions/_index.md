---
title: "Aspose::Words::Loading::TxtLoadOptions Klasse"
linktitle: "TxtLoadOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::TxtLoadOptions Klasse. Ermöglicht das Angeben zusätzlicher Optionen beim Laden eines Textdokuments in ein Document-Objekt. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class


Ermöglicht das Angeben zusätzlicher Optionen beim Laden eines [Text](../../aspose.words/loadformat/) Dokuments in ein [Document](../../aspose.words/document/) Objekt. Weitere Informationen finden Sie im Dokumentationsartikel [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class TxtLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht. |
| [get_AutoNumberingDetection](./get_autonumberingdetection/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob die automatische Nummerierungserkennung beim Laden eines Dokuments durchgeführt wird. Der Standardwert ist **true**. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Liest oder setzt die Zeichenfolge, die verwendet wird, um relative URIs im Dokument bei Bedarf in absolute URIs aufzulösen. Kann **null** oder eine leere Zeichenfolge sein. Standard ist **null**. |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Liest oder setzt, ob Metadatei([Wmf](../) oder [Emf](../)) Bilder in das [Png](../) Bildformat konvertiert werden. |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | Liest oder setzt, ob Formen mit EquationXML in Office [Math](../../aspose.words.math/) Objekte konvertiert werden. |
| [get_DetectHyperlinks](./get_detecthyperlinks/)() const | Gibt an, ob Hyperlinks im Text erkannt werden sollen. Der Standardwert ist **false**. |
| [get_DetectNumberingWithWhitespaces](./get_detectnumberingwithwhitespaces/)() const | Ermöglicht die Angabe, wie nummerierte Listenelemente erkannt werden, wenn das Dokument aus einem Nur-Text-Format importiert wird. Der Standardwert ist **true**. |
| [get_DocumentDirection](./get_documentdirection/)() const | Liest oder setzt die Dokumentausrichtung. Der Standardwert ist [LeftToRight](../documentdirection/). |
| [get_Encoding](../loadoptions/get_encoding/)() const | Liest oder setzt die Kodierung, die zum Laden eines HTML-, TXT- oder CHM-Dokuments verwendet wird, wenn die Kodierung im Dokument nicht angegeben ist. Kann **null** sein. Standard ist **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Ermöglicht das Angeben von Dokument-Schrifteinstellungen. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | Gibt an, ob die OLE-Daten ignoriert werden sollen. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Ermittelt die Spracheinstellungen, die beim Laden des Dokuments verwendet werden. |
| [get_LeadingSpacesOptions](./get_leadingspacesoptions/)() const | Liest oder setzt die bevorzugte Option für die Behandlung von führenden Leerzeichen. Der Standardwert ist [ConvertToIndent](../txtleadingspacesoptions/). |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Gibt das Format des zu ladenden Dokuments an. Standard ist [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Ermöglicht die Angabe, dass der Dokument-Ladevorgang einer bestimmten MS‑Word‑Version entsprechen soll. Standardwert ist [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](../loadoptions/get_password/)() const | Liest oder setzt das Passwort zum Öffnen eines verschlüsselten Dokuments. Kann **null** oder ein leerer String sein. Standard ist **null**. |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Liest oder setzt, ob das INCLUDEPICTURE‑Feld beim Lesen von Microsoft‑Word‑Formaten erhalten bleiben soll. Der Standardwert ist **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Wird beim Laden eines Dokuments aufgerufen und akzeptiert Daten zum Ladefortschritt. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | Definiert, wie das Dokument behandelt werden soll, wenn beim Laden Fehler auftreten. Verwenden Sie diese Eigenschaft, um anzugeben, ob das System versuchen soll, das Dokument wiederherzustellen oder ein anderes definiertes Verhalten zu folgen. Der Standardwert ist [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML oder MHTML importiert wird. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Ermöglicht die Verwendung temporärer Dateien beim Lesen eines Dokuments. Standardmäßig ist diese Eigenschaft **null** und es werden keine temporären Dateien verwendet. |
| [get_TrailingSpacesOptions](./get_trailingspacesoptions/)() const | Liest oder setzt die bevorzugte Option für die Behandlung von nachgestellten Leerzeichen. Der Standardwert ist [Trim](../txttrailingspacesoptions/). |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | Gibt an, ob Felder mit dem **dirty**‑Attribut aktualisiert werden sollen. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Liest oder setzt, ob der aus der Windows‑Registrierung erhaltene LCID‑Wert zur Bestimmung der Standardränder der Seiteneinrichtung verwendet werden soll. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust von Daten- oder Formatierungsgenauigkeit führen könnte. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Initialisiert eine neue Instanz dieser Klasse mit Standardwerten. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | Ein Shortcut, um eine neue Instanz dieser Klasse mit dem angegebenen Passwort zum Laden eines verschlüsselten Dokuments zu initialisieren. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Ein Shortcut, um eine neue Instanz dieser Klasse mit auf die angegebenen Werte gesetzten Eigenschaften zu initialisieren. |
| [set_AutoNumberingDetection](./set_autonumberingdetection/)(bool) | Setter für [Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection](./get_autonumberingdetection/). |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | Setter für [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | Setter für [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Setter für [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_DetectHyperlinks](./set_detecthyperlinks/)(bool) | Setter für [Aspose::Words::Loading::TxtLoadOptions::get_DetectHyperlinks](./get_detecthyperlinks/). |
| [set_DetectNumberingWithWhitespaces](./set_detectnumberingwithwhitespaces/)(bool) | Setter für [Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces](./get_detectnumberingwithwhitespaces/). |
| [set_DocumentDirection](./set_documentdirection/)(Aspose::Words::Loading::DocumentDirection) | Setter für [Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection](./get_documentdirection/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Setter für [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Setter für [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Setter für [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LeadingSpacesOptions](./set_leadingspacesoptions/)(Aspose::Words::Loading::TxtLeadingSpacesOptions) | Setter für [Aspose::Words::Loading::TxtLoadOptions::get_LeadingSpacesOptions](./get_leadingspacesoptions/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Setter für [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Setter für [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Setter für [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Setter für [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Wird beim Laden eines Dokuments aufgerufen und akzeptiert Daten zum Ladefortschritt. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Setter für [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML oder MHTML importiert wird. |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Setter für [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_TrailingSpacesOptions](./set_trailingspacesoptions/)(Aspose::Words::Loading::TxtTrailingSpacesOptions) | Setter für [Aspose::Words::Loading::TxtLoadOptions::get_TrailingSpacesOptions](./get_trailingspacesoptions/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Setter für [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Setter für [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust von Daten- oder Formatierungsgenauigkeit führen könnte. |
| [TxtLoadOptions](./txtloadoptions/)() | Initialisiert eine neue Instanz dieser Klasse mit Standardwerten. |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie Hyperlinks gelesen und angezeigt werden.
```cpp
const System::String inputText = System::String(u"Some links in TXT:\n") + u"https://www.aspose.com/\n" + u"https://docs.aspose.com/words/net/\n";

{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::MemoryStream>();
    System::ArrayPtr<uint8_t> buf = System::Text::Encoding::get_ASCII()->GetBytes(inputText);
    stream->Write(buf, 0, buf->get_Length());
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
    loadOptions->set_DetectHyperlinks(true);

    // Dokument mit Hyperlinks laden.
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Hyperlink-Text ausgeben.
    for (auto&& field : System::IterateOver(doc->get_Range()->get_Fields()))
    {
        std::cout << field->get_Result() << std::endl;
    }

    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_Result().Trim(), u"https://www.aspose.com/");
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Result().Trim(), u"https://docs.aspose.com/words/net/");
}
```

## Siehe auch

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)

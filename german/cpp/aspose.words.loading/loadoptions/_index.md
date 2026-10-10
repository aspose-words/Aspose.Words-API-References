---
title: "Aspose::Words::Loading::LoadOptions Klasse"
linktitle: "LoadOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::LoadOptions Klasse. Ermöglicht das Angeben zusätzlicher Optionen (wie Passwort oder Basis-URI), wenn ein Dokument in ein Document-Objekt geladen wird. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.loading/loadoptions/
---
## LoadOptions class


Ermöglicht das Angeben zusätzlicher Optionen (wie Passwort oder Basis-URI), wenn ein Dokument in ein [Document](../../aspose.words/document/) Objekt geladen wird. Weitere Informationen finden Sie im Dokumentationsartikel [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class LoadOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht. |
| [get_BaseUri](./get_baseuri/)() const | Liest oder setzt die Zeichenfolge, die verwendet wird, um relative URIs im Dokument bei Bedarf in absolute URIs aufzulösen. Kann **null** oder eine leere Zeichenfolge sein. Standard ist **null**. |
| [get_ConvertMetafilesToPng](./get_convertmetafilestopng/)() const | Liest oder setzt, ob Metadatei([Wmf](../) oder [Emf](../)) Bilder in das [Png](../) Bildformat konvertiert werden. |
| [get_ConvertShapeToOfficeMath](./get_convertshapetoofficemath/)() const | Liest oder setzt, ob Formen mit EquationXML in Office [Math](../../aspose.words.math/) Objekte konvertiert werden. |
| [get_Encoding](./get_encoding/)() const | Liest oder setzt die Kodierung, die zum Laden eines HTML-, TXT- oder CHM-Dokuments verwendet wird, wenn die Kodierung im Dokument nicht angegeben ist. Kann **null** sein. Standard ist **null**. |
| [get_FontSettings](./get_fontsettings/)() const | Ermöglicht das Angeben von Dokument-Schrifteinstellungen. |
| [get_IgnoreOleData](./get_ignoreoledata/)() const | Gibt an, ob die OLE-Daten ignoriert werden sollen. |
| [get_LanguagePreferences](./get_languagepreferences/)() const | Ermittelt die Spracheinstellungen, die beim Laden des Dokuments verwendet werden. |
| [get_LoadFormat](./get_loadformat/)() const | Gibt das Format des zu ladenden Dokuments an. Standard ist [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](./get_mswversion/)() const | Ermöglicht die Angabe, dass der Dokument-Ladevorgang einer bestimmten MS‑Word‑Version entsprechen soll. Standardwert ist [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](./get_password/)() const | Liest oder setzt das Passwort zum Öffnen eines verschlüsselten Dokuments. Kann **null** oder ein leerer String sein. Standard ist **null**. |
| [get_PreserveIncludePictureField](./get_preserveincludepicturefield/)() const | Liest oder setzt, ob das INCLUDEPICTURE‑Feld beim Lesen von Microsoft‑Word‑Formaten erhalten bleiben soll. Der Standardwert ist **false**. |
| [get_ProgressCallback](./get_progresscallback/)() const | Wird beim Laden eines Dokuments aufgerufen und akzeptiert Daten zum Ladefortschritt. |
| [get_RecoveryMode](./get_recoverymode/)() const | Definiert, wie das Dokument behandelt werden soll, wenn beim Laden Fehler auftreten. Verwenden Sie diese Eigenschaft, um anzugeben, ob das System versuchen soll, das Dokument wiederherzustellen oder ein anderes definiertes Verhalten zu folgen. Der Standardwert ist [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](./get_resourceloadingcallback/)() const | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML oder MHTML importiert wird. |
| [get_TempFolder](./get_tempfolder/)() const | Ermöglicht die Verwendung temporärer Dateien beim Lesen eines Dokuments. Standardmäßig ist diese Eigenschaft **null** und es werden keine temporären Dateien verwendet. |
| [get_UpdateDirtyFields](./get_updatedirtyfields/)() const | Gibt an, ob Felder mit dem **dirty**‑Attribut aktualisiert werden sollen. |
| [get_UseSystemLcid](./get_usesystemlcid/)() const | Liest oder setzt, ob der aus der Windows‑Registrierung erhaltene LCID‑Wert zur Bestimmung der Standardränder der Seiteneinrichtung verwendet werden soll. |
| [get_WarningCallback](./get_warningcallback/)() const | Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust von Daten- oder Formatierungsgenauigkeit führen könnte. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](./loadoptions/)() | Initialisiert eine neue Instanz dieser Klasse mit Standardwerten. |
| [LoadOptions](./loadoptions/)(const System::String\&) | Ein Shortcut, um eine neue Instanz dieser Klasse mit dem angegebenen Passwort zum Laden eines verschlüsselten Dokuments zu initialisieren. |
| [LoadOptions](./loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Ein Shortcut, um eine neue Instanz dieser Klasse mit auf die angegebenen Werte gesetzten Eigenschaften zu initialisieren. |
| [set_BaseUri](./set_baseuri/)(const System::String\&) | Setter für [Aspose::Words::Loading::LoadOptions::get_BaseUri](./get_baseuri/). |
| [set_ConvertMetafilesToPng](./set_convertmetafilestopng/)(bool) | Setter für [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](./get_convertmetafilestoppng/). |
| [set_ConvertShapeToOfficeMath](./set_convertshapetoofficemath/)(bool) | Setter für [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](./get_convertshapetoofficemath/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Setter für [Aspose::Words::Loading::LoadOptions::get_Encoding](./get_encoding/). |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Setter für [Aspose::Words::Loading::LoadOptions::get_FontSettings](./get_fontsettings/). |
| [set_IgnoreOleData](./set_ignoreoledata/)(bool) | Setter für [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](./get_ignoreoledata/). |
| [set_LoadFormat](./set_loadformat/)(Aspose::Words::LoadFormat) | Setter für [Aspose::Words::Loading::LoadOptions::get_LoadFormat](./get_loadformat/). |
| [set_MswVersion](./set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Setter für [Aspose::Words::Loading::LoadOptions::get_MswVersion](./get_mswversion/). |
| [set_Password](./set_password/)(const System::String\&) | Setter für [Aspose::Words::Loading::LoadOptions::get_Password](./get_password/). |
| [set_PreserveIncludePictureField](./set_preserveincludepicturefield/)(bool) | Setter für [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](./get_preserveincludepicturefield/). |
| [set_ProgressCallback](./set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Wird beim Laden eines Dokuments aufgerufen und akzeptiert Daten zum Ladefortschritt. |
| [set_RecoveryMode](./set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Setter für [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](./get_recoverymode/). |
| [set_ResourceLoadingCallback](./set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML oder MHTML importiert wird. |
| [set_TempFolder](./set_tempfolder/)(const System::String\&) | Setter für [Aspose::Words::Loading::LoadOptions::get_TempFolder](./get_tempfolder/). |
| [set_UpdateDirtyFields](./set_updatedirtyfields/)(bool) | Setter für [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](./get_updatedirtyfields/). |
| [set_UseSystemLcid](./set_usesystemlcid/)(bool) | Setter für [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](./get_usesystemlcid/). |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust von Daten- oder Formatierungsgenauigkeit führen könnte. |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man ein verschlüsseltes Microsoft Word-Dokument lädt.
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// Aspose.Words wirft eine Ausnahme, wenn wir versuchen, ein verschlüsseltes Dokument ohne dessen Passwort zu öffnen.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// Beim Laden eines solchen Dokuments wird das Passwort mithilfe eines LoadOptions-Objekts an den Konstruktor des Dokuments übergeben.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// Es gibt zwei Möglichkeiten, ein verschlüsseltes Dokument mit einem LoadOptions-Objekt zu laden.
// 1 -  Laden Sie das Dokument vom lokalen Dateisystem über den Dateinamen:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  Laden Sie das Dokument aus einem Stream:
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## Siehe auch

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)

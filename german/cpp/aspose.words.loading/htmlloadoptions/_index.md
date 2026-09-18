---
title: "Aspose::Words::Loading::HtmlLoadOptions class"
linktitle: "HtmlLoadOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::HtmlLoadOptions class. Ermöglicht das Angeben zusätzlicher Optionen beim Laden eines HTML-Dokuments in ein Document-Objekt. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class


Ermöglicht das Angeben zusätzlicher Optionen beim Laden eines HTML-Dokuments in ein [Document](../../aspose.words/document/) Objekt. Weitere Informationen finden Sie im Dokumentationsartikel [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class HtmlLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Liest oder setzt die Zeichenfolge, die verwendet wird, um relative URIs im Dokument bei Bedarf in absolute URIs aufzulösen. Kann **null** oder eine leere Zeichenfolge sein. Standard ist **null**. |
| [get_BlockImportMode](./get_blockimportmode/)() const | Liest oder setzt einen Wert, der angibt, wie Eigenschaften von Blockelementen importiert werden. Standardwert ist [Merge](../blockimportmode/). |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Liest oder setzt, ob Metadatei([Wmf](../) oder [Emf](../)) Bilder in das [Png](../) Bildformat konvertiert werden. |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | Liest oder setzt, ob Formen mit EquationXML in Office [Math](../../aspose.words.math/) Objekte konvertiert werden. |
| [get_ConvertSvgToEmf](./get_convertsvgtoemf/)() const | Liest oder setzt einen Wert, der angibt, ob geladene SVG-Bilder in das EMF-Format konvertiert werden. Standardwert ist **false** und, wenn möglich, werden geladene SVG-Bilder unverändert ohne Konvertierung gespeichert. |
| [get_Encoding](../loadoptions/get_encoding/)() const | Liest oder setzt die Kodierung, die zum Laden eines HTML-, TXT- oder CHM-Dokuments verwendet wird, wenn die Kodierung im Dokument nicht angegeben ist. Kann **null** sein. Standard ist **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Ermöglicht das Angeben von Dokument-Schrifteinstellungen. |
| [get_IgnoreNoscriptElements](./get_ignorenoscriptelements/)() const | Liest oder setzt einen Wert, der angibt, ob <noscript>-HTML-Elemente ignoriert werden. Standardwert ist **false**. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | Gibt an, ob die OLE-Daten ignoriert werden sollen. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Ermittelt die Spracheinstellungen, die beim Laden des Dokuments verwendet werden. |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Gibt das Format des zu ladenden Dokuments an. Standard ist [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Ermöglicht die Angabe, dass der Dokument-Ladevorgang einer bestimmten MS‑Word‑Version entsprechen soll. Standardwert ist [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](../loadoptions/get_password/)() const | Liest oder setzt das Passwort zum Öffnen eines verschlüsselten Dokuments. Kann **null** oder ein leerer String sein. Standard ist **null**. |
| [get_PreferredControlType](./get_preferredcontroltype/)() const | Liest oder setzt den bevorzugten Typ von Dokumentknoten, die importierte <input>- und <select>-Elemente darstellen. Standardwert ist [FormField](../htmlcontroltype/). |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Liest oder setzt, ob das INCLUDEPICTURE‑Feld beim Lesen von Microsoft‑Word‑Formaten erhalten bleiben soll. Der Standardwert ist **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Wird beim Laden eines Dokuments aufgerufen und akzeptiert Daten zum Ladefortschritt. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | Definiert, wie das Dokument behandelt werden soll, wenn beim Laden Fehler auftreten. Verwenden Sie diese Eigenschaft, um anzugeben, ob das System versuchen soll, das Dokument wiederherzustellen oder ein anderes definiertes Verhalten zu folgen. Der Standardwert ist [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML oder MHTML importiert wird. |
| [get_SupportFontFaceRules](./get_supportfontfacerules/)() const | Liest oder setzt einen Wert, der angibt, ob @font-face‑Regeln unterstützt und deklarierte Schriften geladen werden sollen. Standardwert ist **false**. |
| [get_SupportVml](./get_supportvml/)() const | Liest oder setzt einen Wert, der angibt, ob VML‑Bilder unterstützt werden. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Ermöglicht die Verwendung temporärer Dateien beim Lesen eines Dokuments. Standardmäßig ist diese Eigenschaft **null** und es werden keine temporären Dateien verwendet. |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | Gibt an, ob Felder mit dem **dirty**‑Attribut aktualisiert werden sollen. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Liest oder setzt, ob der aus der Windows‑Registrierung erhaltene LCID‑Wert zur Bestimmung der Standardränder der Seiteneinrichtung verwendet werden soll. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust von Daten- oder Formatierungsgenauigkeit führen könnte. |
| [get_WebRequestTimeout](./get_webrequesttimeout/)() const | Die Anzahl der Millisekunden, die gewartet wird, bevor die Webanfrage abläuft. Der Standardwert ist 100000 Millisekunden (100 Sekunden). |
| [GetType](./gettype/)() const override |  |
| [HtmlLoadOptions](./htmlloadoptions/)() | Initialisiert eine neue Instanz dieser Klasse mit Standardwerten. |
| [HtmlLoadOptions](./htmlloadoptions/)(const System::String\&) | Ein Shortcut, um eine neue Instanz dieser Klasse mit dem angegebenen Passwort zum Laden eines verschlüsselten Dokuments zu initialisieren. |
| [HtmlLoadOptions](./htmlloadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Ein Shortcut, um eine neue Instanz dieser Klasse mit auf die angegebenen Werte gesetzten Eigenschaften zu initialisieren. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Initialisiert eine neue Instanz dieser Klasse mit Standardwerten. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | Ein Shortcut, um eine neue Instanz dieser Klasse mit dem angegebenen Passwort zum Laden eines verschlüsselten Dokuments zu initialisieren. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Ein Shortcut, um eine neue Instanz dieser Klasse mit auf die angegebenen Werte gesetzten Eigenschaften zu initialisieren. |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | Setter für [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_BlockImportMode](./set_blockimportmode/)(Aspose::Words::Loading::BlockImportMode) | Setter für [Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode](./get_blockimportmode/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | Setter für [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Setter für [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_ConvertSvgToEmf](./set_convertsvgtoemf/)(bool) | Setter für [Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf](./get_convertsvgtoemf/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Setter für [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Setter für [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreNoscriptElements](./set_ignorenoscriptelements/)(bool) | Setter für [Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements](./get_ignorenoscriptelements/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Setter für [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Setter für [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Setter für [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Setter für [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreferredControlType](./set_preferredcontroltype/)(Aspose::Words::Loading::HtmlControlType) | Setter für [Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType](./get_preferredcontroltype/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Setter für [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Wird beim Laden eines Dokuments aufgerufen und akzeptiert Daten zum Ladefortschritt. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Setter für [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML oder MHTML importiert wird. |
| [set_SupportFontFaceRules](./set_supportfontfacerules/)(bool) | Setter für [Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules](./get_supportfontfacerules/). |
| [set_SupportVml](./set_supportvml/)(bool) | Setter für [Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml](./get_supportvml/). |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Setter für [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Setter für [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Setter für [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust von Daten- oder Formatierungsgenauigkeit führen könnte. |
| [set_WebRequestTimeout](./set_webrequesttimeout/)(int32_t) | Die Anzahl der Millisekunden, die gewartet wird, bevor die Webanfrage abläuft. Der Standardwert ist 100000 Millisekunden (100 Sekunden). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie bedingte Kommentare beim Laden eines HTML-Dokuments unterstützt werden.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Wenn der Wert true ist, berücksichtigen wir VML-Code beim Parsen des geladenen Dokuments.
loadOptions->set_SupportVml(supportVml);

// Dieses Dokument enthält ein JPEG-Bild innerhalb von "<!--[if gte vml 1]>"-Tags,
// und ein anderes PNG-Bild innerhalb von "<![if !vml]>"-Tags.
// Wenn wir das Flag "SupportVml" auf "true" setzen, lädt Aspose.Words das JPEG.
// Wenn wir dieses Flag auf "false" setzen, lädt Aspose.Words nur das PNG.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## Siehe auch

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)

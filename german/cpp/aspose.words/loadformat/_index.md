---
title: "Aspose::Words::LoadFormat enum"
linktitle: "LoadFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LoadFormat enum. Gibt das Format des Dokuments an, das in C++ geladen werden soll."
type: docs
weight: 97000
url: /de/cpp/aspose.words/loadformat/
---
## LoadFormat enum


Gibt das Format des zu ladenden Dokuments an.

```cpp
enum class LoadFormat
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Auto | 0 | Weist Aspose.Words an, das Format automatisch zu erkennen. |
| MsWorks | 8 | Microsoft Works 8 [Dokument](../document/). |
| Doc | 10 | Microsoft Word 95 oder Word 97 - 2003 [Dokument](../document/). |
| Dot | 11 | Microsoft Word 95 oder Word 97 - 2003 Vorlage. |
| DocPreWord60 | 12 | Das Dokument liegt im Pre-Word‑95-Format vor. Aspose.Words unterstützt das Laden solcher Dokumente derzeit nicht. |
| Docx | 20 | Office Open XML WordprocessingML [Dokument](../document/) (makrofrei). |
| Docm | 21 | Office Open XML WordprocessingML Makro‑aktiviert [Dokument](../document/). |
| Dotx | 22 | Office Open XML WordprocessingML Vorlage (makrofrei). |
| Dotm | 23 | Office Open XML WordprocessingML Makro‑aktivierte Vorlage. |
| FlatOpc | 24 | Office Open XML WordprocessingML, gespeichert in einer flachen XML‑Datei anstelle eines ZIP‑Pakets. |
| FlatOpcMacroEnabled | 25 | Office Open XML WordprocessingML Makro‑aktiviert [Dokument](../document/) gespeichert in einer flachen XML‑Datei anstelle eines ZIP‑Pakets. |
| FlatOpcTemplate | 26 | Office Open XML WordprocessingML Vorlage (makrofrei) gespeichert in einer flachen XML‑Datei anstelle eines ZIP‑Pakets. |
| FlatOpcTemplateMacroEnabled | 27 | Office Open XML WordprocessingML Makro‑aktivierte Vorlage gespeichert in einer flachen XML‑Datei anstelle eines ZIP‑Pakets. |
| Rtf | 30 | RTF-Format. |
| WordML | 31 | Microsoft Word 2003 WordprocessingML-Format. |
| Html | 50 | HTML-Format. |
| Mhtml | 51 | MHTML (Web-Archiv)-Format. |
| Mobi | 52 | MOBI-Format. Verwendet vom MobiPocket-Leser und von Amazon Kindle-Lesegeräten. |
| Chm | 53 | CHM (Compiled HTML Help)-Format. |
| Azw3 | 54 | AZW3-Format. Verwendet von Amazon Kindle-Lesegeräten. |
| Epub | 55 | EPUB-Format. |
| Odt | 60 | ODF-Text [Document](../document/). |
| Ott | 61 | ODF-Text [Document](../document/) Vorlage. |
| Text | 62 | Einfacher Text. |
| Markdown | 63 | Markdown-Textdokument. |
| Xml | 65 | XML-Dokument. |
| Unknown | 255 | Unbekanntes Format, kann nicht von [Aspose.Words](../) geladen werden. |


## Beispiele



Zeigt, wie die Methoden von [FileFormatUtil](../fileformatutil/) verwendet werden, um das Format eines Dokuments zu erkennen.
```cpp
// Laden Sie ein Dokument aus einer Datei, der die Dateierweiterung fehlt, und erkennen Sie anschließend ihr Dateiformat.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // Nachfolgend sind zwei Methoden zum Konvertieren eines LoadFormat in das entsprechende SaveFormat aufgeführt.
    // 1 -  Erhalte die Dateierweiterungszeichenkette für das LoadFormat und erhalte dann das entsprechende SaveFormat aus dieser Zeichenkette:
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 -  Konvertiere das LoadFormat direkt zu seinem SaveFormat:
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // Lade ein Dokument aus dem Stream und speichere es anschließend mit der automatisch erkannten Dateierweiterung.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```


Zeigt, wie man beim Öffnen eines HTML-Dokuments eine Basis-URI angibt.
```cpp
// Angenommen, wir möchten ein .html-Dokument laden, das ein Bild enthält, das über eine relative URI verlinkt ist
// während sich das Bild an einem anderen Ort befindet. In diesem Fall müssen wir die relative URI in eine absolute URI auflösen.
// Wir können eine Basis-URI mithilfe eines HtmlLoadOptions-Objekts bereitstellen.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Obwohl das Bild im Eingabe-.html beschädigt war, half uns unsere benutzerdefinierte Basis-URI, den Link zu reparieren.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Dieses Ausgabedokument zeigt das fehlende Bild an.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

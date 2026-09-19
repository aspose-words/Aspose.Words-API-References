---
title: "Aspose::Words::LoadFormat enum"
linktitle: "LoadFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Enum Aspose::Words::LoadFormat. Indica il formato del documento da caricare in C++."
type: docs
weight: 97000
url: /it/cpp/aspose.words/loadformat/
---
## LoadFormat enum


Indica il formato del documento da caricare.

```cpp
enum class LoadFormat
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Auto | 0 | Istruisce Aspose.Words a riconoscere automaticamente il formato. |
| MsWorks | 8 | Microsoft Works 8 [Documento](../document/). |
| Doc | 10 | Microsoft Word 95 o Word 97 - 2003 [Documento](../document/). |
| Dot | 11 | Modello Microsoft Word 95 o Word 97 - 2003. |
| DocPreWord60 | 12 | Il documento è in formato pre-Word 95. Aspose.Words attualmente non supporta il caricamento di tali documenti. |
| Docx | 20 | Office Open XML WordprocessingML [Documento](../document/) (senza macro). |
| Docm | 21 | Office Open XML WordprocessingML Abilitato alle macro [Documento](../document/). |
| Dotx | 22 | Modello Office Open XML WordprocessingML (senza macro). |
| Dotm | 23 | Modello Office Open XML WordprocessingML abilitato alle macro. |
| FlatOpc | 24 | Office Open XML WordprocessingML memorizzato in un file XML piatto invece di un pacchetto ZIP. |
| FlatOpcMacroEnabled | 25 | Office Open XML WordprocessingML abilitato alle macro [Documento](../document/) memorizzato in un file XML piatto invece di un pacchetto ZIP. |
| FlatOpcTemplate | 26 | Modello Office Open XML WordprocessingML (senza macro) memorizzato in un file XML piatto invece di un pacchetto ZIP. |
| FlatOpcTemplateMacroEnabled | 27 | Modello Office Open XML WordprocessingML abilitato alle macro memorizzato in un file XML piatto invece di un pacchetto ZIP. |
| Rtf | 30 | Formato RTF. |
| WordML | 31 | Formato Microsoft Word 2003 WordprocessingML. |
| Html | 50 | Formato HTML. |
| Mhtml | 51 | Formato MHTML (archivio web). |
| Mobi | 52 | Formato MOBI. Utilizzato dal lettore MobiPocket e dai lettori Amazon Kindle. |
| Chm | 53 | Formato CHM (Aiuto HTML compilato). |
| Azw3 | 54 | Formato AZW3. Utilizzato dai lettori Amazon Kindle. |
| Epub | 55 | Formato EPUB. |
| Odt | 60 | Testo ODF [Documento](../document/). |
| Ott | 61 | Modello ODF Text [Documento](../document/). |
| Testo | 62 | Testo semplice. |
| Markdown | 63 | Documento di testo Markdown. |
| Xml | 65 | Documento XML. |
| Unknown | 255 | Formato non riconosciuto, non può essere caricato da [Aspose.Words](../). |


## Esempi



Mostra come utilizzare i metodi di [FileFormatUtil](../fileformatutil/) per rilevare il formato di un documento.
```cpp
// Carica un documento da un file a cui manca l'estensione e quindi rileva il suo formato file.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // Di seguito sono riportati due metodi per convertire un LoadFormat nel relativo SaveFormat.
    // 1 -  Ottieni la stringa dell'estensione file per il LoadFormat, quindi ottieni il SaveFormat corrispondente da quella stringa:
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 -  Converti direttamente il LoadFormat nel suo SaveFormat:
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // Carica un documento dallo stream e poi salvalo con l'estensione file rilevata automaticamente.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```


Mostra come specificare un URI di base quando si apre un documento html.
```cpp
// Supponiamo di voler caricare un documento .html che contiene un'immagine collegata tramite un URI relativo
// mentre l'immagine si trova in una posizione diversa. In tal caso, dovremo risolvere l'URI relativo in uno assoluto.
// Possiamo fornire un URI di base usando un oggetto HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Mentre l'immagine era interrotta nell'html di input, il nostro URI di base personalizzato ci ha aiutato a riparare il collegamento.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Questo documento di output visualizzerà l'immagine che mancava.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

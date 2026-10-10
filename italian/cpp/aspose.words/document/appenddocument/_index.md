---
title: "Aspose::Words::Document::AppendDocument metodo"
linktitle: "AppendDocument"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::AppendDocument metodo. Aggiunge il documento specificato alla fine di questo documento in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words/document/appenddocument/
---
## Document::AppendDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) method


Aggiunge il documento specificato alla fine di questo documento.

```cpp
void Aspose::Words::Document::AppendDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Il documento da aggiungere. |
| importFormatMode | Aspose::Words::ImportFormatMode | Specifica come unire la formattazione degli stili che entra in conflitto. |

## Esempi



Mostra come aggiungere un documento alla fine di un altro documento.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
srcDoc->get_FirstSection()->get_Body()->AppendParagraph(u"Source document text. ");

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
dstDoc->get_FirstSection()->get_Body()->AppendParagraph(u"Destination document text. ");

// Aggiungi il documento di origine al documento di destinazione mantenendo la sua formattazione,
// quindi salva il documento di origine nel file system locale.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting);

dstDoc->Save(get_ArtifactsDir() + u"Document.AppendDocument.docx");
```


Mostra come aggiungere tutti i documenti in una cartella alla fine di un documento modello.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Template Document");
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Normal);
builder->Writeln(u"Some content here");

// Aggiungi tutti i documenti non crittografati con estensione .doc
// dalla nostra directory del file system locale al documento base.
System::SharedPtr<System::Collections::Generic::List<System::String>> docFiles = System::IO::Directory::GetFiles(get_MyDir(), u"*.doc")->LINQ_Where(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String item)>>([](System::String item) -> bool
{
    return item.EndsWith(u".doc");
})))->LINQ_ToList();
for (auto&& fileName : docFiles)
{
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(fileName);
    if (info->get_IsEncrypted())
    {
        continue;
    }

    auto srcDoc = System::MakeObject<Aspose::Words::Document>(fileName);
    dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles);
}

dstDoc->Save(get_ArtifactsDir() + u"Document.AppendAllDocumentsInFolder.doc");
```

## Vedi anche

* Class [Document](../)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::AppendDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


Aggiunge il documento specificato alla fine di questo documento.

```cpp
void Aspose::Words::Document::AppendDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Il documento da aggiungere. |
| importFormatMode | Aspose::Words::ImportFormatMode | Specifica come unire la formattazione degli stili che entra in conflitto. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Consente di specificare opzioni che influenzano la formattazione di un documento risultato. |

## Esempi



Mostra come gestire i conflitti di stile delle liste durante l'aggiunta di un documento.
```cpp
// Carica un documento con testo in uno stile personalizzato e clonalo.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom list numbering.docx");
System::SharedPtr<Aspose::Words::Document> dstDoc = srcDoc->Clone();

// Ora abbiamo due documenti, ciascuno con uno stile identico chiamato "CustomStyle".
// Modifica il colore del testo per uno degli stili per distinguerlo dall'altro.
dstDoc->get_Styles()->idx_get(u"CustomStyle")->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

// Se c'è un conflitto di stili di lista, applica il formato di lista del documento di origine.
// Imposta la proprietà "KeepSourceNumbering" su "false" per non importare alcun numero di lista nel documento di destinazione.
// Imposta la proprietà "KeepSourceNumbering" su "true" per importare tutti i conflitti
// la numerazione dello stile di lista con lo stesso aspetto che aveva nel documento di origine.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_KeepSourceNumbering(keepSourceNumbering);

// Unire due documenti che hanno stili diversi con lo stesso nome provoca un conflitto di stile.
// Possiamo specificare una modalità di importazione del formato durante l'aggiunta di documenti per risolvere questo conflitto.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepDifferentStyles, options);
dstDoc->UpdateListLabels();

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```


Mostra come gestire i conflitti di stile delle liste durante l'inserimento di un documento.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

dstDoc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);
System::SharedPtr<Aspose::Words::Lists::List> list = dstDoc->get_Lists()->idx_get(0);

builder->get_ListFormat()->set_List(list);

for (int32_t i = 1; i <= 15; i++)
{
    builder->Write(System::String::Format(u"List Item {0}\n", i));
}

auto attachDoc = System::ExplicitCast<Aspose::Words::Document>(System::ExplicitCast<Aspose::Words::Node>(dstDoc)->Clone(true));

// Se c'è un conflitto di stili di lista, applica il formato di lista del documento di origine.
// Imposta la proprietà "KeepSourceNumbering" su "false" per non importare alcun numero di lista nel documento di destinazione.
// Imposta la proprietà "KeepSourceNumbering" su "true" per importare tutti i conflitti
// la numerazione dello stile di lista con lo stesso aspetto che aveva nel documento di origine.
auto importOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importOptions->set_KeepSourceNumbering(keepSourceNumbering);

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->InsertDocument(attachDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importOptions);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```


Mostra come gestire i conflitti di stile delle liste durante l'aggiunta di un clone di un documento a se stesso.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// Se c'è un conflitto di stili di lista, applica il formato di lista del documento di origine.
// Imposta la proprietà "KeepSourceNumbering" su "false" per non importare alcun numero di lista nel documento di destinazione.
// Imposta la proprietà "KeepSourceNumbering" su "true" per importare tutti i conflitti
// la numerazione dello stile di lista con lo stesso aspetto che aveva nel documento di origine.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_KeepSourceNumbering(keepSourceNumbering);
builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->UpdateListLabels();
```

## Vedi anche

* Class [Document](../)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

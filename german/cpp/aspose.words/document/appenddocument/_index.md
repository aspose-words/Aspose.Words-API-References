---
title: "Aspose::Words::Document::AppendDocument Methode"
linktitle: "AppendDocument"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::AppendDocument Methode. Fügt das angegebene Dokument am Ende dieses Dokuments in C++ an."
type: docs
weight: 5000
url: /de/cpp/aspose.words/document/appenddocument/
---
## Document::AppendDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) method


Fügt das angegebene Dokument am Ende dieses Dokuments an.

```cpp
void Aspose::Words::Document::AppendDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Das anzuhängende Dokument. |
| importFormatMode | Aspose::Words::ImportFormatMode | Gibt an, wie sich widersprechende Formatierungen zusammengeführt werden. |

## Beispiele



Zeigt, wie man ein Dokument am Ende eines anderen Dokuments anhängt.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
srcDoc->get_FirstSection()->get_Body()->AppendParagraph(u"Source document text. ");

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
dstDoc->get_FirstSection()->get_Body()->AppendParagraph(u"Destination document text. ");

// Hängen Sie das Quelldokument an das Zieldokument an, wobei dessen Formatierung beibehalten wird,
// und speichern Sie anschließend das Quelldokument im lokalen Dateisystem.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting);

dstDoc->Save(get_ArtifactsDir() + u"Document.AppendDocument.docx");
```


Zeigt, wie man alle Dokumente in einem Ordner an das Ende eines Vorlagendokuments anhängt.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Template Document");
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Normal);
builder->Writeln(u"Some content here");

// Alle unverschlüsselten Dokumente mit der .doc-Erweiterung anhängen
// aus unserem lokalen Dateisystemverzeichnis zum Basisdokument.
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

## Siehe auch

* Class [Document](../)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::AppendDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


Fügt das angegebene Dokument am Ende dieses Dokuments an.

```cpp
void Aspose::Words::Document::AppendDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Das anzuhängende Dokument. |
| importFormatMode | Aspose::Words::ImportFormatMode | Gibt an, wie sich widersprechende Formatierungen zusammengeführt werden. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Ermöglicht das Festlegen von Optionen, die die Formatierung eines Ergebnisdokuments beeinflussen. |

## Beispiele



Zeigt, wie man Listenvorlagenkonflikte beim Anhängen eines Dokuments verwaltet.
```cpp
// Lädt ein Dokument mit Text in einem benutzerdefinierten Stil und klont es.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom list numbering.docx");
System::SharedPtr<Aspose::Words::Document> dstDoc = srcDoc->Clone();

// Wir haben jetzt zwei Dokumente, jedes mit einem identischen Stil namens "CustomStyle".
// Ändern Sie die Textfarbe eines der Stile, um ihn vom anderen zu unterscheiden.
dstDoc->get_Styles()->idx_get(u"CustomStyle")->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

// Falls ein Konflikt von Listenvorlagen besteht, wenden Sie das Listenformat des Quelldokuments an.
// Setzen Sie die Eigenschaft "KeepSourceNumbering" auf "false", um keine Listennummern in das Zieldokument zu importieren.
// Setzen Sie die Eigenschaft "KeepSourceNumbering" auf "true", um alle kollidierenden
// Listenvorlagen-Nummerierung mit dem gleichen Aussehen wie im Quelldokument zu importieren.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_KeepSourceNumbering(keepSourceNumbering);

// Das Zusammenführen zweier Dokumente, die unterschiedliche Stile mit demselben Namen besitzen, verursacht einen Stilkonflikt.
// Wir können beim Anhängen von Dokumenten einen Importformatmodus angeben, um diesen Konflikt zu lösen.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepDifferentStyles, options);
dstDoc->UpdateListLabels();

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```


Zeigt, wie man Listenvorlagenkonflikte beim Einfügen eines Dokuments verwaltet.
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

// Falls ein Konflikt von Listenvorlagen besteht, wenden Sie das Listenformat des Quelldokuments an.
// Setzen Sie die Eigenschaft "KeepSourceNumbering" auf "false", um keine Listennummern in das Zieldokument zu importieren.
// Setzen Sie die Eigenschaft "KeepSourceNumbering" auf "true", um alle kollidierenden
// Listenvorlagen-Nummerierung mit dem gleichen Aussehen wie im Quelldokument zu importieren.
auto importOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importOptions->set_KeepSourceNumbering(keepSourceNumbering);

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->InsertDocument(attachDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importOptions);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```


Zeigt, wie man Listenvorlagenkonflikte beim Anhängen einer Kopie eines Dokuments an sich selbst verwaltet.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// Falls ein Konflikt von Listenvorlagen besteht, wenden Sie das Listenformat des Quelldokuments an.
// Setzen Sie die Eigenschaft "KeepSourceNumbering" auf "false", um keine Listennummern in das Zieldokument zu importieren.
// Setzen Sie die Eigenschaft "KeepSourceNumbering" auf "true", um alle kollidierenden
// Listenvorlagen-Nummerierung mit dem gleichen Aussehen wie im Quelldokument zu importieren.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_KeepSourceNumbering(keepSourceNumbering);
builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->UpdateListLabels();
```

## Siehe auch

* Class [Document](../)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

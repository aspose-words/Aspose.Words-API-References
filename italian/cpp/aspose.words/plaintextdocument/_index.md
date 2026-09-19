---
title: "Classe Aspose::Words::PlainTextDocument"
linktitle: "PlainTextDocument"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::PlainTextDocument. Consente di estrarre la rappresentazione in testo semplice del contenuto del documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 50000
url: /it/cpp/aspose.words/plaintextdocument/
---
## PlainTextDocument class


Consente di estrarre la rappresentazione in testo semplice del contenuto del documento. Per saperne di più, visita l'articolo di documentazione [Working with Text Document](https://docs.aspose.com/words/cpp/working-with-text-document/).

```cpp
class PlainTextDocument : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | Ottiene [BuiltInDocumentProperties](./get_builtindocumentproperties/) del documento. |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() const | Ottiene [CustomDocumentProperties](./get_customdocumentproperties/) del documento. |
| [get_Text](./get_text/)() const | Ottiene il contenuto testuale del documento concatenato in una stringa. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&) | Crea un documento di testo semplice da un file. Rileva automaticamente il formato del file. |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Crea un documento di testo semplice da un file. Consente di specificare opzioni aggiuntive come una password di crittografia. |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&) | Crea un documento di testo semplice da uno stream. Rileva automaticamente il formato del file. |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Crea un documento di testo semplice da uno stream. Consente di specificare opzioni aggiuntive come una password di crittografia. |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&) |  |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |
| static [Type](./type/)() |  |

## Esempi



Mostra come caricare il contenuto di un documento Microsoft Word in testo semplice.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

---
title: "Costruttore Aspose::Words::NodeImporter::NodeImporter"
linktitle: "NodeImporter"
second_title: "Riferimento API Aspose.Words per C++"
description: "Costruttore Aspose::Words::NodeImporter::NodeImporter. Inizializza una nuova istanza della classe NodeImporter in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter::NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) constructor


Inizializza una nuova istanza della classe [NodeImporter](../).

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Il documento di origine. |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Il documento di destinazione che sarà il proprietario dei nodi importati. |
| importFormatMode | Aspose::Words::ImportFormatMode | Specifica come unire la formattazione degli stili che entra in conflitto. |

## Vedi anche

* Class [DocumentBase](../../documentbase/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## NodeImporter::NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) constructor


Inizializza una nuova istanza della classe [NodeImporter](../).

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Il documento di origine. |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Il documento di destinazione che sarà il proprietario dei nodi importati. |
| importFormatMode | Aspose::Words::ImportFormatMode | Specifica come unire la formattazione degli stili che entra in conflitto. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Specifica varie opzioni per formattare il nodo importato. |

## Esempi



Mostra come risolvere un conflitto durante l'importazione di documenti che contengono elenchi con lo stesso identificatore di definizione dell'elenco.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - destination.docx");

// Imposta la proprietà "KeepSourceNumbering" su "true" per applicare un ID di definizione dell'elenco diverso
// a stili identici come Aspose.Words li importa nei documenti di destinazione.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(true);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, importFormatOptions);
dstDoc->UpdateListLabels();
```


Mostra come risolvere i conflitti di numerazione degli elenchi nei documenti di origine e di destinazione.
```cpp
// Apri un documento con uno schema di numerazione dell'elenco personalizzato, quindi clonalo.
// Poiché entrambi hanno lo stesso formato di numerazione, i formati entreranno in conflitto se importiamo un documento nell'altro.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom list numbering.docx");
System::SharedPtr<Aspose::Words::Document> dstDoc = srcDoc->Clone();

// Quando importiamo il clone del documento nell'originale e poi lo aggiungiamo,
// allora i due elenchi con lo stesso formato di elenco si uniranno.
// Se impostiamo il flag "KeepSourceNumbering" su "false", allora l'elenco dal clone del documento
// che aggiungiamo all'originale continuerà la numerazione dell'elenco a cui lo aggiungiamo.
// Ciò unirà efficacemente i due elenchi in uno solo.
// Se impostiamo il flag "KeepSourceNumbering" su "true", allora il clone del documento
// l'elenco conserverà la sua numerazione originale, facendo apparire i due elenchi come elenchi separati.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(keepSourceNumbering);

auto importer = System::MakeObject<Aspose::Words::NodeImporter>(srcDoc, dstDoc, Aspose::Words::ImportFormatMode::KeepDifferentStyles, importFormatOptions);
for (auto&& paragraph : System::IterateOver<Aspose::Words::Paragraph>(srcDoc->get_FirstSection()->get_Body()->get_Paragraphs()))
{
    System::SharedPtr<Aspose::Words::Node> importedNode = importer->ImportNode(paragraph, true);
    dstDoc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Node>>(importedNode);
}

dstDoc->UpdateListLabels();

if (keepSourceNumbering)
{
    ASSERT_EQ(System::String(u"6. Item 1\r\n") + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4\r\n" + u"6. Item 1\r\n" + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4", dstDoc->get_FirstSection()->get_Body()->ToString(Aspose::Words::SaveFormat::Text).Trim());
}
else
{
    ASSERT_EQ(System::String(u"6. Item 1\r\n") + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4\r\n" + u"10. Item 1\r\n" + u"11. Item 2 \r\n" + u"12. Item 3\r\n" + u"13. Item 4", dstDoc->get_FirstSection()->get_Body()->ToString(Aspose::Words::SaveFormat::Text).Trim());
}
```

## Vedi anche

* Class [DocumentBase](../../documentbase/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

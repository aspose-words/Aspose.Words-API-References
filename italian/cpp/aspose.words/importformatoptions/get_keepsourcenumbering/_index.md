---
title: "Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering metodo"
linktitle: "get_KeepSourceNumbering"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering metodo. Ottiene o imposta un valore booleano che specifica come la numerazione verrà importata quando entra in conflitto nei documenti di origine e di destinazione. Il valore predefinito è false in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words/importformatoptions/get_keepsourcenumbering/
---
## ImportFormatOptions::get_KeepSourceNumbering method


Ottiene o imposta un valore booleano che specifica come verrà importata la numerazione quando entra in conflitto nei documenti di origine e destinazione. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering() const
```


## Esempi



Mostra come importare un documento con elenchi numerati.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List destination.docx");

ASSERT_EQ(4, dstDoc->get_Lists()->get_Count());

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();

// Se c'è un conflitto di stili di lista, applica il formato di lista del documento di origine.
// Imposta la proprietà "KeepSourceNumbering" su "false" per non importare alcun numero di lista nel documento di destinazione.
// Imposta la proprietà "KeepSourceNumbering" su "true" per importare tutti i conflitti
// la numerazione dello stile di lista con lo stesso aspetto che aveva nel documento di origine.
options->set_KeepSourceNumbering(isKeepSourceNumbering);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);
dstDoc->UpdateListLabels();

ASSERT_EQ(isKeepSourceNumbering ? 5 : 4, dstDoc->get_Lists()->get_Count());
```


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

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Aspose::Words::NodeImporter::NodeImporter konstruktor"
linktitle: "NodeImporter"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::NodeImporter::NodeImporter konstruktor. Initierar en ny instans av NodeImporter‑klassen i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter::NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) constructor


Initierar en ny instans av klassen [NodeImporter](../).

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Källdokumentet. |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Destinationsdokumentet som kommer att vara ägare till importerade noder. |
| importFormatMode | Aspose::Words::ImportFormatMode | Anger hur stilformatering som krockar ska slås samman. |

## Se även

* Class [DocumentBase](../../documentbase/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## NodeImporter::NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) constructor


Initierar en ny instans av klassen [NodeImporter](../).

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Källdokumentet. |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Destinationsdokumentet som kommer att vara ägare till importerade noder. |
| importFormatMode | Aspose::Words::ImportFormatMode | Anger hur stilformatering som krockar ska slås samman. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Anger olika alternativ för att formatera importerad nod. |

## Exempel



Visar hur man löser en krock när man importerar dokument som har listor med samma listdefinitionidentifierare.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - destination.docx");

// Ställ in egenskapen "KeepSourceNumbering" till "true" för att tillämpa ett annat listdefinitions‑ID
// till identiska stilar som Aspose.Words importerar dem till destinationsdokument.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(true);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, importFormatOptions);
dstDoc->UpdateListLabels();
```


Visar hur man löser krockar i listnumrering i käll- och destinationsdokument.
```cpp
// Öppna ett dokument med ett anpassat listnumreringsschema, och klona det sedan.
// Eftersom båda har samma numreringsformat, kommer formaten att krocka om vi importerar ett dokument till det andra.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom list numbering.docx");
System::SharedPtr<Aspose::Words::Document> dstDoc = srcDoc->Clone();

// När vi importerar dokumentets klon till originalet och sedan lägger till det,
// kommer de två listorna med samma listformat att slås ihop.
// Om vi sätter flaggan "KeepSourceNumbering" till "false", så blir listan från dokumentklonen
// som vi lägger till i originalet kommer att fortsätta numreringen av listan vi lägger till den i.
// Detta kommer effektivt att slå samman de två listorna till en.
// Om vi sätter flaggan "KeepSourceNumbering" till "true", så blir dokumentklonen
// listan kommer att bevara sin ursprungliga numrering, vilket får de två listorna att visas som separata listor.
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

## Se även

* Class [DocumentBase](../../documentbase/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

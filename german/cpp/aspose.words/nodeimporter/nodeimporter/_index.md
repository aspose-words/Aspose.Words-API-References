---
title: "Aspose::Words::NodeImporter::NodeImporter-Konstruktor"
linktitle: "NodeImporter"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::NodeImporter::NodeImporter-Konstruktor. Initialisiert eine neue Instanz der Klasse NodeImporter in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter::NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) constructor


Initialisiert eine neue Instanz der Klasse [NodeImporter](../).

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Das Quell-Dokument. |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Das Ziel-Dokument, das Eigentümer der importierten Knoten sein wird. |
| importFormatMode | Aspose::Words::ImportFormatMode | Gibt an, wie sich widersprechende Formatierungen zusammengeführt werden. |

## Siehe auch

* Class [DocumentBase](../../documentbase/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## NodeImporter::NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) constructor


Initialisiert eine neue Instanz der Klasse [NodeImporter](../).

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Das Quell-Dokument. |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Das Ziel-Dokument, das Eigentümer der importierten Knoten sein wird. |
| importFormatMode | Aspose::Words::ImportFormatMode | Gibt an, wie sich widersprechende Formatierungen zusammengeführt werden. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Gibt verschiedene Optionen zum Formatieren des importierten Knotens an. |

## Beispiele



Zeigt, wie ein Konflikt beim Importieren von Dokumenten gelöst wird, die Listen mit derselben Listendefinitionskennung besitzen.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - destination.docx");

// Setzen Sie die "KeepSourceNumbering"-Eigenschaft auf "true", um eine andere Listendefinitions-ID anzuwenden
// zu identischen Formaten, wie Aspose.Words sie in Zieldokumente importiert.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(true);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, importFormatOptions);
dstDoc->UpdateListLabels();
```


Zeigt, wie Listennummerierungskonflikte in Quell- und Zieldokumenten gelöst werden können.
```cpp
// Öffnen Sie ein Dokument mit einem benutzerdefinierten Listennummerierungsschema und klonen Sie es anschließend.
// Da beide dasselbe Nummerierungsformat haben, kollidieren die Formate, wenn wir ein Dokument in das andere importieren.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom list numbering.docx");
System::SharedPtr<Aspose::Words::Document> dstDoc = srcDoc->Clone();

// Wenn wir die Kopie des Dokuments in das Original importieren und sie dann anhängen,
// werden die beiden Listen mit demselben Listenformat zusammengeführt.
// Wenn wir das "KeepSourceNumbering"-Flag auf "false" setzen, dann wird die Liste aus der Dokumentkopie
// die wir an das Original anhängen, die Nummerierung der Ziel-Liste fortführen.
// Damit werden die beiden Listen effektiv zu einer zusammengeführt.
// Wenn wir das "KeepSourceNumbering"-Flag auf "true" setzen, dann wird die Dokumentkopie
// die ihre ursprüngliche Nummerierung beibehält, sodass die beiden Listen als separate Listen erscheinen.
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

## Siehe auch

* Class [DocumentBase](../../documentbase/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

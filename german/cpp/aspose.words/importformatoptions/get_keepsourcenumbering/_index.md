---
title: "Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering-Methode"
linktitle: "get_KeepSourceNumbering"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering-Methode. Gibt einen booleschen Wert zurück oder legt ihn fest, der angibt, wie die Nummerierung importiert wird, wenn sie in Quell- und Zieldokumenten kollidiert. Der Standardwert ist false in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words/importformatoptions/get_keepsourcenumbering/
---
## ImportFormatOptions::get_KeepSourceNumbering method


Liest oder setzt einen booleschen Wert, der festlegt, wie die Nummerierung importiert wird, wenn sie in Quell‑ und Zieldokumenten kollidiert. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering() const
```


## Beispiele



Zeigt, wie ein Dokument mit nummerierten Listen importiert wird.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List destination.docx");

ASSERT_EQ(4, dstDoc->get_Lists()->get_Count());

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();

// Falls ein Konflikt von Listenvorlagen besteht, wenden Sie das Listenformat des Quelldokuments an.
// Setzen Sie die Eigenschaft "KeepSourceNumbering" auf "false", um keine Listennummern in das Zieldokument zu importieren.
// Setzen Sie die Eigenschaft "KeepSourceNumbering" auf "true", um alle kollidierenden
// Listenvorlagen-Nummerierung mit dem gleichen Aussehen wie im Quelldokument zu importieren.
options->set_KeepSourceNumbering(isKeepSourceNumbering);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);
dstDoc->UpdateListLabels();

ASSERT_EQ(isKeepSourceNumbering ? 5 : 4, dstDoc->get_Lists()->get_Count());
```


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

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

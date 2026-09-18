---
title: "Aspose::Words::Document::get_LastSection method"
linktitle: "get_LastSection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_LastSection-Methode. Ruft den letzten Abschnitt im Dokument in C++ ab."
type: docs
weight: 35000
url: /de/cpp/aspose.words/document/get_lastsection/
---
## Document::get_LastSection method


Liest den letzten Abschnitt im Dokument.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Document::get_LastSection()
```


## Beispiele



Zeigt, wie man mit einem Document Builder einen neuen Abschnitt erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ein leeres Dokument enthält standardmäßig einen Abschnitt,
// der Kindknoten enthält, die wir bearbeiten können.
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// Verwenden Sie einen Document Builder, um Text zum ersten Abschnitt hinzuzufügen.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Erstellen Sie einen zweiten Abschnitt, indem Sie einen Abschnittsumbruch einfügen.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(2, doc->get_Sections()->get_Count());

// Jeder Abschnitt hat seine eigenen Seiteneinrichtungseinstellungen.
// Wir können den Text im zweiten Abschnitt in zwei Spalten aufteilen.
// Dies wirkt sich nicht auf den Text im ersten Abschnitt aus.
doc->get_LastSection()->get_PageSetup()->get_TextColumns()->SetCount(2);
builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

ASSERT_EQ(1, doc->get_FirstSection()->get_PageSetup()->get_TextColumns()->get_Count());
ASSERT_EQ(2, doc->get_LastSection()->get_PageSetup()->get_TextColumns()->get_Count());

doc->Save(get_ArtifactsDir() + u"Section.Create.docx");
```

## Siehe auch

* Class [Section](../../section/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

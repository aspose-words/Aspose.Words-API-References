---
title: "Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting Methode"
linktitle: "get_ContextTableFormatting"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting Methode. True, wenn die auf Tabelleninhalt angewendete Formatierung die Formatierung des nachfolgenden Inhalts nicht beeinflusst. Der Standardwert ist true in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words/documentbuilderoptions/get_contexttableformatting/
---
## DocumentBuilderOptions::get_ContextTableFormatting method


Wahr, wenn die auf den Tabelleninhalt angewandte Formatierung die Formatierung des nachfolgenden Inhalts nicht beeinflusst. Standardwert ist **true**.

```cpp
bool Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting() const
```


## Beispiele



Zeigt, wie die Tabellenformatierung für nachfolgenden Inhalt ignoriert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// Fügt Inhalt vor der Tabelle hinzu.
// Standard-Schriftgröße ist 12.
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// Ändert die Schriftgröße innerhalb der Tabelle.
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// Wenn ContextTableFormatting wahr ist, wird die Tabellenformatierung nicht auf den nachfolgenden Inhalt angewendet.
// Wenn ContextTableFormatting falsch ist, wird die Tabellenformatierung auf den nachfolgenden Inhalt angewendet.
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## Siehe auch

* Class [DocumentBuilderOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

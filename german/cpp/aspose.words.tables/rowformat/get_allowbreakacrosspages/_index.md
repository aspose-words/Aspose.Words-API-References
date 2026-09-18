---
title: "Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages-Methode"
linktitle: "get_AllowBreakAcrossPages"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages-Methode. Wahr, wenn der Text in einer Tabellenzeile über einen Seitenumbruch hinweg aufgeteilt werden darf in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.tables/rowformat/get_allowbreakacrosspages/
---
## RowFormat::get_AllowBreakAcrossPages method


True, wenn der Text in einer Tabellenzeile über einen Seitenumbruch hinweg aufgeteilt werden darf.

```cpp
bool Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages()
```


## Beispiele



Zeigt, wie man das Zeilenumbruch‑Über‑Seiten‑Verhalten für jede Zeile in einer Tabelle deaktiviert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Setzen Sie die Eigenschaft \"AllowBreakAcrossPages\" auf \"false\", um die Zeile
// in einem Stück zu halten, wenn eine Tabelle über zwei Seiten reicht, die entlang dieser Zeile aufgeteilt werden.
// Wenn die Zeile zu groß ist, um auf eine Seite zu passen, schiebt Microsoft Word sie auf die nächste Seite.
// Setzen Sie die Eigenschaft \"AllowBreakAcrossPages\" auf \"true\", um zu erlauben, dass die Zeile über zwei Seiten hinweg umbricht.
for (auto&& row : System::IterateOver<Aspose::Words::Tables::Row>(table))
{
    row->get_RowFormat()->set_AllowBreakAcrossPages(allowBreakAcrossPages);
}

doc->Save(get_ArtifactsDir() + u"Table.AllowBreakAcrossPages.docx");
```

## Siehe auch

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

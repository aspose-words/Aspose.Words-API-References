---
title: "Aspose::Words::TableStyle::get_Alignment metodo"
linktitle: "get_Alignment"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TableStyle::get_Alignment metodo. Specifica l'allineamento per lo stile della tabella in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/tablestyle/get_alignment/
---
## TableStyle::get_Alignment method


Specifica l'allineamento per lo stile di tabella.

```cpp
Aspose::Words::Tables::TableAlignment Aspose::Words::TableStyle::get_Alignment()
```


## Esempi



Mostra come impostare la posizione di una tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono due modi per allineare orizzontalmente una tabella.
// 1 -  Usa la proprietà "Alignment" per allinearla a una posizione nella pagina, come il centro:
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

// Inserisci una tabella e applica lo stile che abbiamo creato.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Aligned to the center of the page");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

table->set_Style(tableStyle);

// 2 -  Usa la "LeftIndent" per specificare un rientro dal margine sinistro della pagina:
tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle2"));
tableStyle->set_LeftIndent(55);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Green());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Aligned according to left indent");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

table->set_Style(tableStyle);

doc->Save(get_ArtifactsDir() + u"Table.SetTableAlignment.docx");
```

## Vedi anche

* Enum [TableAlignment](../../../aspose.words.tables/tablealignment/)
* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

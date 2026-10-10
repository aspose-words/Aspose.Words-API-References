---
title: "Aspose::Words::Tables::Row::get_Hidden método"
linktitle: "get_Hidden"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Tables::Row::get_Hidden. Obtiene o establece una bandera que indica si esta fila está oculta o no en C++."
type: docs
weight: 6500
url: /es/cpp/aspose.words.tables/row/get_hidden/
---
## Row::get_Hidden method


Obtiene o establece una bandera que indica si esta fila está oculta o no.

```cpp
bool Aspose::Words::Tables::Row::get_Hidden()
```


## Ejemplos



Muestra cómo ocultar una fila de tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Row> row = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0)->get_FirstRow();
row->set_Hidden(true);

doc->Save(get_ArtifactsDir() + u"Table.HiddenRow.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Table.HiddenRow.docx");

row = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0)->get_FirstRow();
ASSERT_TRUE(row->get_Hidden());

for (auto&& cell : System::IterateOver<Aspose::Words::Tables::Cell>(row->get_Cells()))
{
    for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(cell->get_Paragraphs()))
    {
        for (auto&& run : System::IterateOver<Aspose::Words::Run>(para->get_Runs()))
        {
            ASSERT_TRUE(run->get_Font()->get_Hidden());
        }
    }
}
```

## Ver también

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

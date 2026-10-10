---
title: "Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout‑metod"
linktitle: "get_PreserveTableLayout"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout‑metod. Anger om programmet ska försöka bevara tabellernas layout när det sparas i vanligt textformat. Standardvärdet är falskt i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.saving/txtsaveoptions/get_preservetablelayout/
---
## TxtSaveOptions::get_PreserveTableLayout method


Anger om programmet ska försöka bevara tabellernas layout vid sparande i vanligt textformat. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout() const
```


## Exempel



Visar hur man bevarar tabellernas layout när man konverterar till vanlig text.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1");
builder->InsertCell();
builder->Write(u"Row 1, cell 2");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1");
builder->InsertCell();
builder->Write(u"Row 2, cell 2");
builder->EndTable();

// Skapa ett \"TxtSaveOptions\"-objekt, som vi kan skicka till dokumentets \"Save\"-metod
// för att ändra hur vi sparar dokumentet som ren text.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Ställ in egenskapen "PreserveTableLayout" till "true" för att applicera mellanslagspaddning på innehållet
// i det resulterande vanliga textdokumentet för att bevara så mycket av tabellens layout som möjligt.
// Ställ in egenskapen "PreserveTableLayout" till "false" för att spara alla tabellers innehåll
// som en kontinuerlig textmassa, med bara en ny rad för varje rad.
txtSaveOptions->set_PreserveTableLayout(preserveTableLayout);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
{
    ASSERT_EQ(System::String(u"Row 1, cell 1                                            Row 1, cell 2\r\n") + u"Row 2, cell 1                                            Row 2, cell 2\r\n\r\n", docText);
}
else
{
    ASSERT_EQ(System::String(u"Row 1, cell 1\r") + u"Row 1, cell 2\r" + u"Row 2, cell 1\r" + u"Row 2, cell 2\r\r\n", docText);
}
```

## Se även

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

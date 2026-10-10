---
title: "Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels metod"
linktitle: "get_SimplifyListLabels"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels metod. Anger om programmet ska förenkla listetiketter när komplex etikettformatering inte kan representeras tillräckligt av vanlig text. Om den är satt till true skrivs numrerade listetiketter i ett enkelt numeriskt format och punktlistor som enkla ASCII-tecken. Standardvärdet är false i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.saving/txtsaveoptions/get_simplifylistlabels/
---
## TxtSaveOptions::get_SimplifyListLabels method


Anger om programmet ska förenkla listetiketter när komplex etikettformatering inte kan representeras tillräckligt i vanlig text. Om den sätts till **true** skrivs numrerade listetiketter i ett enkelt numeriskt format och punktlistetiketter som enkla ASCII‑tecken. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels() const
```


## Exempel



Visar hur man ändrar utseendet på listor när man sparar ett dokument som ren text.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa en punktlista med fem indenteringsnivåer.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 3");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 4");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 5");

// Skapa ett \"TxtSaveOptions\"-objekt, som vi kan skicka till dokumentets \"Save\"-metod
// för att ändra hur vi sparar dokumentet som ren text.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Ställ in egenskapen "SimplifyListLabels" till "true" för att konvertera vissa list
// symboler till enklare ASCII-tecken, såsom '*', 'o', '+', '>', etc.
// Ställ in egenskapen "SimplifyListLabels" till "false" för att bevara så många ursprungliga listsymboler som möjligt.
txtSaveOptions->set_SimplifyListLabels(simplifyListLabels);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.SimplifyListLabels.txt");

System::String newLine = System::Environment::get_NewLine();
if (simplifyListLabels)
{
    ASSERT_EQ(System::String::Format(u"* Item 1{0}", newLine) + System::String::Format(u"  > Item 2{0}", newLine) + System::String::Format(u"    + Item 3{0}", newLine) + System::String::Format(u"      - Item 4{0}", newLine) + System::String::Format(u"        o Item 5{0}", newLine), docText);
}
else
{
    ASSERT_EQ(System::String::Format(u"· Item 1{0}", newLine) + System::String::Format(u"o Item 2{0}", newLine) + System::String::Format(u"§ Item 3{0}", newLine) + System::String::Format(u"· Item 4{0}", newLine) + System::String::Format(u"o Item 5{0}", newLine), docText);
}
```

## Se även

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
